# 🎧 Dissonance (Electron Desktop App)

**Protecting your audio from AI exploitation—now as a downloadable desktop web app.**

---

## 🔒 About

Dissonance is now a cross-platform desktop app built with Electron and web technologies. It helps defend audio content from unauthorized use in AI training, recognition, and synthesis, using imperceptible adversarial perturbations.

---

## 💡 Core Goals

- Provide a user-friendly desktop app for audio protection
- Use web technologies for rapid development and cross-platform support
- Allow users to customize protection levels and process audio files locally

---

## 🧰 Tech Stack

- **Frontend:** HTML, CSS, JavaScript (React planned)
- **Desktop Packaging:** Electron
- **Build Tools:** electron-builder

## 🚀 Continuous Integration & Deployment

### CI/CD Pipeline

This repository uses **GitHub Actions** to automate building and packaging the Electron desktop app. On every push or pull request to the `main` branch, the workflow will:

- Install dependencies
- Build the Electron app
- Package installers for Windows, macOS, and Linux

You can find the workflow file at `.github/workflows/electron-app.yml` (to be created).

### Deployment & Hosting

- Downloadable installers will be published to **GitHub Releases** for each new version.
- Optionally, a project website will provide download links.

---

## 🏗️ Two-Repo Architecture

This project uses a two-repo workflow:

- **Core Repo:** Contains the algorithm and audio processing logic. Exposes functionality as a native library or WebAssembly (WASM) module.
- **App Repo (this repo):** Electron/web app that pulls the core artifact for its functionality.

### How Integration Works
1. The core repo builds and publishes its artifact (native library or WASM) to GitHub Releases, npm, or a public URL.
2. The app repo fetches the latest core artifact during build (using a script, npm package, or Git submodule).
3. The Electron app loads and uses the core functionality via Node.js bindings or WASM.

### Example Integration (WASM)
- Place the core WASM file in `dissonance-app/core/`.
- Load it in your frontend code:
  ```js
  import initCore from './core/core_wasm.js';
  // Use core functions after initialization
  ```

### Example Integration (Native Node.js Addon)
- Place the compiled native library in `dissonance-app/core/`.
- Load it in your backend code:
  ```js
  const core = require('./core/core_native.node');
  // Use core functions
  ```

### CI/CD
- Core repo: Builds and publishes the artifact.
- App repo: Fetches the artifact, builds the app, runs tests, and packages installers.

---

## 📣 Get Involved

We welcome feedback, collaboration, and testers for our upcoming builds. Join the discussion:

- 💬 [Discord Community](https://discord.gg/QdKd8WKG8V)

---

## 📜 License & Ethics

- Comply with GDPR, CCPA, and ethical data use standards
- Share research insights and results
- Engage transparently with the open-source and audio communities

---
