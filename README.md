# Pomodoro Timer

A single-file, vanilla HTML/CSS/JS Pomodoro timer with daily session history.

## How to run

No build step, no dependencies, no server required.

```bash
# Option 1 — just open the file
open index.html

# Option 2 — serve locally (avoids any browser quirks with file:// and localStorage)
npx serve .
# then visit http://localhost:3000

# Option 3 — Python one-liner
python3 -m http.server 8080
# then visit http://localhost:8080
```

Requires: a modern browser (Chrome 90+, Firefox 88+, Safari 14+). No Node, no npm install needed for Option 1.

## Features

- **Focus + break timer** — configurable from 1–90 min focus, 1–30 min break
- **Smooth ring animation** — SVG stroke-dashoffset ticks down in real time
- **Audible chime** — three-note ascending chord via Web Audio API on session end
- **Auto-transition** — moves from focus → break → focus automatically
- **Daily history** — persists in `localStorage`, resets on a new calendar day
- **Keyboard shortcut** — `Space` to start/pause when focused on the page
- **Two visual modes** — dark warm (focus) ↔ light green (break), animated transition
