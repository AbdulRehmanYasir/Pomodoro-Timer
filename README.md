<div align="center">

# 🍅 Pomodoro Timer

### Focus Better. Work Smarter. Stay Consistent.

A lightweight, single-file Pomodoro timer built with **HTML, CSS, and JavaScript**, featuring configurable focus and break sessions, smooth animations, audible notifications, and persistent daily history.

</div>

---

## 📖 Overview

**Pomodoro Timer** is a simple, dependency-free productivity timer designed around the Pomodoro technique.

It provides configurable focus and break sessions while keeping a record of completed sessions for the current day.

The entire project is contained in a single HTML file and requires **no build tools, frameworks, or npm dependencies**.

## ✨ Core Features

* ⏱️ **Focus & Break Timer** — Configure focus sessions from 1–90 minutes and breaks from 1–30 minutes.
* 🎨 **Animated Timer Ring** — SVG-based progress ring updates smoothly as time passes.
* 🔔 **Audible Notifications** — Plays a three-note ascending chime when a session ends.
* 🔄 **Automatic Transitions** — Automatically switches between focus and break sessions.
* 📊 **Daily Session History** — Completed sessions are stored using `localStorage`.
* ⌨️ **Keyboard Shortcut** — Press `Space` to start or pause the timer.
* 🌙 **Two Visual Modes** — Warm dark focus mode and light green break mode.
* 💾 **Persistent Data** — Session history remains available across browser refreshes.
* 📱 **Lightweight & Responsive** — No frameworks or external dependencies required.

## 🧠 How It Works

The timer follows a simple Pomodoro cycle:

```text
Focus
  ↓
Break
  ↓
Focus
  ↓
Break
  ↓
...

When a session ends, the application automatically switches to the next session type and plays an audible notification.

Completed focus sessions are recorded in the browser using localStorage and displayed as daily history.

🛠️ Technology Stack
HTML5
CSS3
Vanilla JavaScript
SVG
Web Audio API
localStorage

No React, frameworks, package managers, or external libraries are required.

📂 Project Structure
pomodoro-timer/
│
├── index.html
└── README.md

The complete application is contained inside index.html.

🚀 Running Locally
Option 1 — Open Directly

Simply open:

index.html

in a modern web browser.

Option 2 — Using npx serve
npx serve .

Then open:

http://localhost:3000
Option 3 — Using Python
python3 -m http.server 8080

Then open:

http://localhost:8080

Requirements: A modern web browser such as Chrome 90+, Firefox 88+, or Safari 14+.

Node.js and npm are not required when opening the HTML file directly.

🎯 Learning Objectives

This project was built to practice fundamental frontend concepts, including:

DOM manipulation
JavaScript timers
Event handling
Browser storage
localStorage
SVG animations
Web Audio API
Keyboard events
State management with vanilla JavaScript
Responsive UI design
CSS transitions and animations
🔮 Future Improvements

Possible future additions include:

Custom notification sounds
Long-break support
Configurable session cycles
Weekly productivity statistics
Exportable session history
Browser notifications
Dark/light theme controls
Custom themes
Productivity charts
Task integration
👨‍💻 Author

Abdul Rehman Yasir

BS Artificial Intelligence Student

GitHub: AbdulRehmanYasir

<div align="center">
Keep Learning. Keep Building. Keep Improving.

Pomodoro Timer — Simple Focus, Consistent Progress.

Made with ❤️ by Abdul Rehman Yasir

</div> ```
