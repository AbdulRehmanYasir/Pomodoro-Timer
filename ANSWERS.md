# ANSWERS.md

## 1. How to run

No build step required — it's a single `index.html` file.

```bash
# Fastest: just open it
open index.html

# Or serve locally to avoid any file:// quirks
npx serve .
# → http://localhost:3000
```

No npm install, no Node version requirement. Works in any modern browser (Chrome 90+, Firefox 88+, Safari 14+).

---

## 2. Stack & design choices

**Stack:** Vanilla HTML, CSS, and JavaScript — no framework, no build tool. The entire app is one file. For a Pomodoro timer the state is simple (a counter, a phase flag, a list), so a framework would add ceremony without value. The single-file approach also means zero configuration for whoever reviews it.

**Visual decision 1 — The ring takes ~65% of the viewport width.**
The ring is the timer. I sized it to `min(66vw, 300px)` so it dominates the screen on both phone and desktop. The point of a Pomodoro timer is ambient awareness — you glance at it while working — and a large ring communicates "how much is left" without the user having to read the number. The number is there for precision; the ring is there for feel. A smaller ring would make the timer feel like a widget; this size makes it feel like the *room's mood*.

**Visual decision 2 — Two full-body color themes (dark/warm for focus, light/green for break).**
Most Pomodoro apps just swap a label that says "Break time." I made the entire page theme shift: focus is a near-black background with amber accents; break is a pale sage-green with forest accents. The transition is 0.6s eased, so it washes across the screen. This serves a real functional purpose — at a glance, from across a desk, you can see which mode you're in without reading anything. The color contrast is also emotionally tuned: amber-on-black feels focused and pressured (good for work); green-on-white feels open and calm (good for rest).

---

## 3. Responsive & accessibility

**360px phone:** The ring scales to `75vw`, the controls stack naturally in a row with reduced padding, and the settings panel stacks its rows vertically. The history list has `max-height: 200px` with `overflow-y: auto` so it never pushes content off-screen. Text never goes below 11px.

**1440px laptop:** Max-width is 520px centered, so the timer stays compact and readable rather than stretching across the full viewport. Wide screens don't help a countdown timer — the constraint keeps it feeling intentional rather than sparse.

**Accessibility handled — keyboard navigation and focus states:**
Every interactive element (buttons, settings +/− buttons, the settings toggle) has `:focus-visible` outlines using the current accent color, so keyboard users always know where they are. The `Space` key starts/pauses the timer when focus is on `document.body`, mirroring how media players work. ARIA roles are in place: the timer has `role="timer"`, the mode label has `aria-live="polite"`, the session count updates are exposed to screen readers, and each history item has an `aria-label` with the full readable string ("Completed 25:00 focus session at 3:42pm").

**Accessibility skipped — reduced motion:**
I didn't add `@media (prefers-reduced-motion: reduce)` to disable the ring animation and theme transition. For a non-critical animation app this is a real gap — users with vestibular disorders or motion sensitivities would get the full animated experience. With another day I'd wrap all `transition` and `animation` declarations in a `prefers-reduced-motion` media query and replace the ring with a static numeric countdown for those users.

---

## 4. AI usage

**Tool used:** Claude (this conversation).

**What I asked:** I used Claude to scaffold the SVG ring math (stroke-dasharray / stroke-dashoffset calculation), the Web Audio API tone sequence, and the initial CSS variable architecture.

**What I changed — the ring progress direction:**
Claude's initial ring code rotated the `<svg>` element using a CSS class, but it applied `transform: rotate(-90deg)` to the entire element including the text. The timer digits ended up upside-down. I moved the rotation to only the SVG `<svg>` element directly (which contains only the `<circle>` elements) and kept the text overlay as an absolutely-positioned `<div>` outside the SVG entirely. This is a more robust separation anyway — SVG text rendering across browsers is inconsistent, and having the display as a DOM element means it inherits CSS variables for color transitions correctly.

**What I changed — the audio chord:**
Claude gave me a single sine-wave beep at 440Hz. I replaced it with a three-note ascending arpeggio (C5, E5, G5) with 220ms stagger and an exponential gain ramp-down on each note. The original beep was jarring and felt like an error sound. The chord feels like an achievement — it's the same interval structure used in "level complete" sounds in games. I also wrapped the entire function in a try/catch because Web Audio context creation can fail silently in some sandboxed environments.

---

## 5. Honest gap

**The settings don't persist across reloads.**

If a user sets focus to 45 minutes, reloads the page, and comes back, the timer resets to the default 25/5. The history survives (it's in `localStorage`) but the configured durations don't. This is a meaningful UX gap — the whole point of customization is that it sticks.

The fix is straightforward: on every settings change, write `{focusMin, breakMin}` to `localStorage` alongside the history object, and read it back on initialization before calling `updateDisplay()`. I'd also want to validate the stored values (clamp them to the 1–90 range) in case of corrupted storage. About 20 lines of code and 15 minutes of work — I just ran out of time to wire it up cleanly.
