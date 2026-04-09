# 🌙 Glazing Mocha — YASB Status Bar Theme

> *A dark, minimal, glass-and-grain status bar experience powered by Catppuccin Mocha.*

---

## ✨ Preview

> Screenshots from the config showcase:

  | Widget | Preview |
  |--------|---------|
  | Yasb Bar| [Bar] (/assets/yasb_bar_yasb-bar_20260406_004705.png) |
  | AI Chat | ![AI Chat](/assets/yasb_widget_showcase_ai-chat.png) |
  | Memory Popup | ![Memory](/assets/yasb_widget_showcase_memory.png) |
  | Notes | ![Notes](/assets/yasb_widget_showcase_notes.png) |
  | Todo | ![Todo](/assets/yasb_widget_showcase_todo.png) |

---

## 🎨 Design Philosophy

**Glazing Mocha** is a carefully crafted YASB theme built around the [Catppuccin Mocha](https://github.com/catppuccin/catppuccin) palette. Every widget breathes with:

- 🌑 Deep, translucent backgrounds using `rgba` layering
- ✨ Acrylic blur effects on the bar and all popups
- 💜 Lavender and mauve accent highlights
- 🔤 JetBrainsMono Nerd Font Propo at 12–13px for crisp monospace readability
- 🌈 Semantic color states: green → yellow → peach → red for system metrics
- ✨ Smooth `fadeInOut` animations on every widget interaction

---

## 🧩 Widget Lineup

### Left Side
| Widget | Description |
|--------|-------------|
| ⚡ Power Menu | Full-screen power overlay with user profile |
| 📝 Notes | Floating note-taking with rich text support |
| ✅ Todo | Task manager with categories (Urgent, Important, Soon, Today) |
| 🗑️ Recycle Bin | Live item count with fill/empty icons |
| 🤖 AI Chat | Ollama-powered local LLM chat (Qwen 3.5, Qwen Coder) |
| 🪟 GlazeWM Workspaces | Tiling WM workspace switcher with scroll support |

### Center
| Widget | Description |
|--------|-------------|
| 🧠 CPU | Usage % with graph popup and Task Manager shortcut |
| 🎮 GPU | GPU utilization with temp popup (index 0) |
| 🍅 Pomodoro | Timer with circular progress menu, work/break indicators |
| 💾 Memory | RAM usage % with graph popup |
| 💿 Disk | C: drive usage with threshold color states |

### Right Side
| Widget | Description |
|--------|-------------|
| 🔔 Notifications | Windows notification count with badge |
| 🔧 Systray | Collapsible system tray with pin-click modifier |
| 🖼️ Wallpapers | Gallery picker (4 per page, portrait, lazy-load) |
| ☀️ Brightness | Toggle slider with icon levels |
| 📶 Bluetooth | Connected device name with Settings shortcut |
| 🌐 WiFi | Signal strength icon, hides when Ethernet active |
| 🌤️ Weather | Open-Meteo widget (no API key needed) with hourly card |
| 🔊 Volume | Level + mute with per-app audio sliders |
| 🕐 Clock | `HH:MM` with calendar popup on right-click |

---

## 🛠️ Requirements

- [YASB](https://github.com/amnweb/yasb) — Yet Another Status Bar
- [GlazeWM](https://github.com/glzr-io/glazewm) — Tiling window manager
- [Ollama](https://ollama.com/) — Local AI (for AI Chat widget)
- [JetBrainsMono Nerd Font Propo](https://github.com/ryanoasis/nerd-fonts/releases/latest/download/JetBrainsMono.zip)
- Windows 11 (for acrylic blur and round corners)

---

## 🚀 Installation

1. **Clone or download** this config
2. Copy `config.yaml` and `styles.css` to:
   ```
   C:/Users/{username}/.config/yasb/
   ```
3. Update the wallpaper path in `config.yaml`:
   ```yaml
   image_path: "C:/path/to/your/Wallpapers"
   ```
4. Replace `{username}` in any paths with your Windows username
5. Start YASB:
   ```powershell
   yasbc start
   ```

---

## ⚙️ Customization

### Change AI Provider
Edit the `ai_chat` widget's `providers` block to add OpenAI, GitHub Copilot, or any OpenAI-compatible API.

### Change Disk Volume
Update `volume_label: "C"` in the `disk` widget to your preferred drive letter.

### GitHub Notifications
Uncomment the `github` widget and set your token (or use `YASB_GITHUB_TOKEN` env var).

### Weather Location
The Open-Meteo widget auto-detects location via its built-in geocoder — click the widget to set your city.

---

## 🎨 Color Palette

All colors are defined as CSS variables for easy customization:

```css
--base:     #1e1e2e   /* Background */
--lavender: #b4befe   /* Primary accent */
--mauve:    #cba6f7   /* Purple highlight */
--blue:     #89b4fa   /* Info / links */
--green:    #a6e3a1   /* Success / low usage */
--yellow:   #f9e2af   /* Warning / medium usage */
--peach:    #fab387   /* Caution / high usage */
--red:      #f38ba8   /* Critical / error */
--teal:     #94e2d5   /* Volume / secondary accent */
```

---

## 📜 License

MIT — use freely, credit appreciated.

---

<p align="center">
  Made with 💜 and Catppuccin Mocha &nbsp;•&nbsp; Powered by <a href="https://github.com/amnweb/yasb">YASB</a>
</p>
