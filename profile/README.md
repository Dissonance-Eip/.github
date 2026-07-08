# 🎧 Dissonance

**Protecting audio from unauthorized AI training and exploitation — as a local, cross-platform desktop app.**

---

## 🔒 About

Dissonance is a desktop application that helps creators defend their audio from being used to train or drive AI models (recognition, synthesis, voice cloning). It applies perturbations that aim to be **imperceptible to humans** while **disrupting how AI models interpret the sound**. All processing runs locally on the user's machine — audio never leaves the device.

---

## 💡 Goals

- A user-friendly desktop app for audio protection
- Perturbations that stay inaudible to people but confuse AI models
- Fully local, on-device processing

---

## 🧰 Tech Stack

- **Desktop app (`ui`):** Electron + plain HTML/CSS/JavaScript (ES modules), Tailwind CSS
- **Audio engine (`core`):** C++, compiled to a Node.js native addon (`.node`) **and** a CLI
- **Validation (`Tester`):** Python + PyTorch, running real AI models to measure effectiveness
- **Packaging:** electron-builder

---

## 🗂️ Repositories

- **[ui](https://github.com/Dissonance-Eip/ui)** — the Electron desktop app: import a file, edit WAV metadata, choose a protection level, process, compare original vs protected, and export.
- **[core](https://github.com/Dissonance-Eip/core)** — the C++ audio engine, exposed as a Node.js native addon (consumed by the UI) and a CLI (for power users, testing, and evidence). Exports `process`, `readMetadata`, and `writeTags`.
- **[Tester](https://github.com/Dissonance-Eip/Tester)** — a Python harness that scores a perturbation on the two axes that matter: **human inaudibility** (SNR) and **AI confusion** (speech-to-text, genre classification, and a music-encoder model). Also hosts the adversarial-perturbation research.
- **[docs](https://github.com/Dissonance-Eip/docs)** — research, planning, and technical documentation.

---

## 🏗️ How it fits together

Dissonance is split into a **lightweight app** and a **high-performance engine**:

1. **core** builds the C++ audio engine and publishes platform binaries (`.node`) to GitHub Releases via CI.
2. **ui** automatically syncs the latest core binaries into the app, then packages installers.
3. At runtime the Electron app loads the native addon and calls it to read metadata, process audio, and write results — entirely on-device.

The **Tester** closes the loop: it runs audio through real AI models (Whisper for lyrics, MERT for music encoding, MAEST for genre) to measure whether a perturbation is both inaudible and genuinely disruptive to AI — guiding development of the protection method.

---

## ⚙️ Continuous Integration

- **ui** — lint, formatting, unit tests, and a packaging build run on every push / PR; a sync workflow pulls the latest `core` binaries into the app.
- **core** — static analysis, formatting, and C++ unit tests on every push / PR; tagged releases build and publish native addons for Windows, macOS, and Linux.

---

## 📣 Get Involved

We welcome feedback, collaboration, and testers.

- 💬 [Discord Community](https://discord.gg/QdKd8WKG8V)

---

## 📜 License & Ethics

- Comply with GDPR, CCPA, and ethical data-use standards
- Share research insights and results
- Engage transparently with the open-source and audio communities

---
