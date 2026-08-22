<div align="center">
🍅 Pomodoro Timer
Focus Better. Work Smarter. Stay Consistent.

A lightweight, single-file Pomodoro timer built with HTML, CSS, and JavaScript, featuring configurable focus and break sessions, smooth animations, audible notifications, and persistent daily history.

</div>
📖 Overview

Pomodoro Timer is a simple, dependency-free productivity timer designed around the Pomodoro technique.

It provides configurable focus and break sessions while keeping a record of completed sessions for the current day.

The entire project is contained in a single HTML file and requires no build tools, frameworks, or npm dependencies.

✨ Core Features
⏱️ Focus & Break Timer — Configure focus sessions from 1–90 minutes and breaks from 1–30 minutes.
🎨 Animated Timer Ring — SVG-based progress ring updates smoothly as time passes.
🔔 Audible Notifications — Plays a three-note ascending chime when a session ends.
🔄 Automatic Transitions — Automatically switches between focus and break sessions.
📊 Daily Session History — Completed sessions are stored using localStorage.
⌨️ Keyboard Shortcut — Press Space to start or pause the timer.
🌙 Two Visual Modes — Warm dark focus mode and light green break mode.
💾 Persistent Data — Session history remains available across browser refreshes.
📱 Lightweight & Responsive — No frameworks or external dependencies required.
🧠 How It Works

The timer follows a simple cycle:

Focus
  ↓
Break
  ↓
Focus
  ↓
Break
  ↓
...

When a session finishes, the timer automatically transitions to the next session type and plays an audible notification.

Daily completed-session history is stored locally in the browser using localStorage.

🛠️ Technology Stack
HTML5
CSS3
Vanilla JavaScript
SVG
Web Audio API
localStorage

No React, framework, package manager, or external library is required.

📂 Project Structure
pomodoro-timer/
│
├── index.html
└── README.md

The complete application is contained inside index.html.

🚀 How to Run
Option 1 — Open Directly

Download or clone the repository and open:

index.html

in any modern web browser.

Option 2 — Using VS Code
Clone the repository.
Open the project folder in Visual Studio Code.
Open index.html.
Run it using the browser or the Live Server extension.
Option 3 — Using npx serve
npx serve .

Then visit:

http://localhost:3000
Option 4 — Using Python
python3 -m http.server 8080

Then visit:

http://localhost:8080
Requirements

A modern browser is recommended:

Chrome 90+
Firefox 88+
Safari 14+

Node.js and npm are not required when opening the HTML file directly.

📱 Responsive Design

The timer is designed to work across different screen sizes.

The interface adapts to:

Desktop screens
Laptop screens
Tablets
Mobile devices

The timer controls, session information, history, and visual elements remain accessible on smaller screens.

💾 Data & Storage

The application uses the browser's built-in localStorage API to store daily session history.

No external database or backend server is required.

User data remains stored locally in the browser.

🔊 Audio

When a focus or break session ends, the application generates an audible three-note ascending chime using the Web Audio API.

No external audio files are required.

⌨️ Keyboard Controls
Key	Action
Space	Start / Pause timer

The keyboard shortcut allows the timer to be controlled without using the mouse.

🎯 Learning Objectives

This project was built to practice fundamental frontend development concepts, including:

Semantic HTML
CSS styling
Responsive design
DOM manipulation
JavaScript event handling
JavaScript timers
State management with vanilla JavaScript
localStorage
SVG graphics
SVG animations
CSS transitions
Web Audio API
Keyboard events
Browser APIs
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
Sound controls
Session goals
Productivity streaks
📌 Project Status

Completed

The current version provides a functional Pomodoro timer with focus sessions, break sessions, automatic transitions, session history, keyboard controls, animations, and audio notifications.

👨‍💻 Author

Abdul Rehman Yasir

BS Artificial Intelligence Student

GitHub: https://github.com/AbdulRehmanYasir

<div align="center">
Keep Learning. Keep Building. Keep Improving.

Pomodoro Timer — Simple Focus, Consistent Progress.

Made with ❤️ by Abdul Rehman Yasir

</div>
