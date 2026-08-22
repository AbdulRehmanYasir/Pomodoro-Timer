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

The timer follows a simple cycle:

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
