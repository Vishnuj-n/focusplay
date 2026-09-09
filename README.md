<p align="center">
  <img src="logo.png" width="200" alt="FocusPlay Logo">
</p>

<h1 align="center">FocusPlay</h1>

<p align="center">
  <strong>Lock In with Your Own Offline Music • Zero Streaming Distractions • Local Pomodoro Engine</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-blue?style=flat-square" alt="Platform">
  <img src="https://img.shields.io/badge/Go-1.23+-00ADD8?style=flat-square&logo=go" alt="Go">
  <img src="https://img.shields.io/badge/Wails-v2-DF1A29?style=flat-square" alt="Wails">
  <img src="https://img.shields.io/badge/Audio-100%25%20Offline-success?style=flat-square" alt="Offline Audio">
</p>

---

## 🎧 Why FocusPlay?

Most Pomodoro apps force you into generic lo-fi streams, require internet access, or make you fiddle with external browser tabs and Spotify playlists that break your flow.

**FocusPlay is built around your own local audio vault.** Whether you need that single legendary soundtrack looping endlessly for intense coding sprints or an entire directory of instrumental tracks on shuffle, FocusPlay gives you pure offline immersion with zero lag and zero online distractions.

> **Plug in your headphones, point to your local tracks or folders, and dial directly into the zone.**

---

## ✨ Key Highlights

### 🎵 1. Bring Your Own Music (100% Offline)
- **Seamless Single-Track Looping**: Lock into hyper-focus by putting your favorite track or ambient soundscape on a continuous, seamless loop.
- **Folder Shuffle & Playlists**: Point FocusPlay to any local music directory (`.mp3`) and let it shuffle through your study/focus soundtrack.
- **Work vs. Break Soundtracks**: Automatically switch audio modes—e.g., high-focus synthwave during work intervals and calming ambient soundscapes during breaks.
- **Zero Internet / Zero Ads**: Works completely offline. No buffering, no subscriptions, no algorithmic recommendations pulling you away from work.

### ⏱️ 2. Distraction-Free Pomodoro Engine
- **Mini Timer Overlay**: Switch to an ultra-compact, always-on-top mini widget (`M`) that floats discreetly over your IDE or workspace.
- **Custom Profiles**: Configure tailor-made profiles (e.g., *"Deep Work"*, *"Bug Bashing"*, *"Writing"*, *"Reading"*) with unique timers and audio assignments.
- **Session Persistence**: Never lose your momentum. Progress is automatically saved across restarts.
- **Smart Automations**: Configurable auto-start intervals, auto-play audio transitions, and native desktop notifications.

---

## ⌨️ Keyboard Shortcuts

Stay on your keyboard without touching the mouse:

| Shortcut | Action |
| :--- | :--- |
| <kbd>Space</kbd> | Start / Pause Timer |
| <kbd>Esc</kbd> | Stop / Reset Timer |
| <kbd>S</kbd> | Skip current session or break |
| <kbd>M</kbd> | Toggle Minimal Floating Mini-Timer Mode |

---

## 🚀 Quick Start & Installation

### Windows Installer
1. Download the latest installer from [Releases](https://github.com/Vishnuj-n/focusplay/releases) (or grab `build/bin/focusplay.exe`).
2. Run the `.exe` installer.
3. Launch **FocusPlay** and select your music folder or loop track.

---

### 🛠️ Building from Source

#### Prerequisites
- **Go 1.23+**
- **Node.js 18+** & npm
- **Wails CLI**: `go install github.com/wailsapp/wails/v2/cmd/wails@latest`

#### Build Steps
```bash
# 1. Clone repository
git clone https://github.com/Vishnuj-n/focusplay.git
cd focusplay

# 2. Install dependencies
go mod tidy
cd frontend && npm install && cd ..

# 3. Run live development mode
wails dev

# 4. Or compile a production binary (Windows)
wails build --nsis
```

---

## 📂 Project Structure

```
├── build/             # Build artifacts and NSIS installer configs
├── docs/              # Detailed guides (INSTALLATION.md, USAGE.md, etc.)
├── frontend/          # Vite + Vanilla JS UI (HTML, CSS, JS)
│   ├── src/           # UI components, themes, and audio controllers
│   └── wailsjs/       # Auto-generated Go-to-JS bridge
├── internal/          # Core Go backend
│   ├── app/           # App lifecycle & Wails bindings
│   ├── services/      # Audio (beep engine), Timer, and Persistence
│   └── infra/         # Storage and event bus
└── main.go            # Application entrypoint
```

---

## 📖 Documentation

- **[USAGE.md](docs/USAGE.md)**: Full guide to profiles, music configuration, and custom themes.
- **[INSTALLATION.md](docs/INSTALLATION.md)**: Detailed platform build guides (macOS / Linux / Windows).
- **[CONTRIBUTING.md](docs/CONTRIBUTING.md)**: Contribution guidelines and architecture notes.
- **[CHANGELOG.md](docs/CHANGELOG.md)**: Version release notes.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
