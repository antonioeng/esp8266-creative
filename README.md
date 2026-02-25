# ⚡ ESP8266 Creative

A **cyberpunk neon** redesign of the ESP8266 simulator. Same powerful Arduino emulation engine, completely reimagined with glassmorphism, animated backgrounds, particle effects, and a neon cyberpunk aesthetic.

🔗 **Live Demo:** [antonioeng.github.io/esp8266-creative](https://antonioeng.github.io/esp8266-creative/)

> _"A digital art installation / futuristic hacker playground / neon cyberpunk laboratory"_

---

## ✨ Features

- **Cyberpunk Neon UI** — Deep void backgrounds, neon purple/cyan/pink/green glow effects, glassmorphism panels
- **Animated Backgrounds** — Floating blob gradients, particle star fields, scanline overlays
- **Monaco Code Editor** — Full-featured editor with Arduino/C++ syntax highlighting and neon-styled toolbar
- **Real-time Simulation** — Execute `setup()` and `loop()` cycles directly in the browser
- **GPIO & PWM Support** — `pinMode`, `digitalWrite`, `digitalRead`, `analogRead`, `analogWrite` with neon glow brightness
- **Serial Monitor** — Cyberpunk terminal with scanline effects and colour-coded log output
- **Neon Board** — NodeMCU PCB reimagined in deep blue-purple with neon trace lines and glowing components
- **Theme Toggle** — "Neon Lab" (dark) / "Digital Dream" (light) modes
- **Project Management** — Auto-save, rename, export/import `.ino` files

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| UI Framework | React 19 |
| Build Tool | Vite 7 |
| State Management | Zustand |
| Code Editor | Monaco Editor (`@monaco-editor/react`) |
| Styling | CSS Custom Properties + Cyberpunk Neon Design System |
| Fonts | Orbitron · Space Grotesk · JetBrains Mono |
| Deployment | GitHub Pages via GitHub Actions |

## 🚀 Getting Started

### Prerequisites

- Node.js 18+
- npm 9+

### Install & Run

```bash
git clone https://github.com/antonioeng/esp8266emulator.git
cd esp8266emulator
npm install
npm run dev
```

Open [http://localhost:5173/esp8266emulator/](http://localhost:5173/esp8266emulator/) in your browser.

### Build for Production

```bash
npm run build
npm run preview
```

## 📁 Project Structure

```
src/
├── engine/
│   ├── eventBus.js          # Pub/Sub event system
│   ├── gpioManager.js       # GPIO & PWM pin management
│   ├── parser.js            # Arduino C++ → JavaScript transpiler
│   └── simulatorEngine.js   # Simulation orchestrator
├── components/
│   ├── Board/
│   │   ├── ESP8266Board.jsx # NodeMCU board visualization
│   │   ├── LED.jsx          # PWM-aware LED component
│   │   └── Pin.jsx          # GPIO pin with tooltip
│   ├── Editor/
│   │   └── CodeEditor.jsx   # Monaco editor + toolbar
│   └── Console/
│       └── Terminal.jsx      # Serial monitor output
├── store/
│   └── useSimulatorStore.js # Zustand global state
├── services/
│   ├── projectService.js    # Save/load/autosave
│   └── serialService.js     # WebSerial bridge (optional)
├── App.jsx                  # Root layout & theme management
└── index.css                # Theme variables (Catppuccin)
```

## 🎮 Supported Arduino API

| Category | Functions |
|----------|-----------|
| GPIO | `pinMode()`, `digitalWrite()`, `digitalRead()` |
| Analog | `analogRead()`, `analogWrite()` (PWM 0–1023) |
| Serial | `Serial.begin()`, `Serial.print()`, `Serial.println()` |
| Timing | `delay()`, `millis()`, `micros()` |
| Constants | `HIGH`, `LOW`, `OUTPUT`, `INPUT`, `INPUT_PULLUP`, `LED_BUILTIN` |
| Types | `int`, `long`, `bool`, `uint8_t`, `uint16_t`, `uint32_t`, `String`, `size_t` |

## 📝 License

MIT

## 👤 Author

**antonioeng** — [GitHub](https://github.com/antonioeng)
