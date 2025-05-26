# 🎧 Dissonance

**Protecting your audio from AI exploitation—without compromising the sound.**

---

## 🔒 About

**Dissonance** is an early-stage research and software project aimed at defending audio content from unauthorized use in AI training, recognition, and synthesis. Inspired by tools like *Nightshade* and *Fawkes* for image protection, Dissonance applies imperceptible adversarial perturbations to audio files—disrupting how AI models perceive them, while preserving the sound for human listeners.

> *Silencing AI, Preserving Sound*

---

## 💡 Core Goals

- Develop a tool that adds AI-resistant adversarial perturbations to audio
- Keep audio quality unchanged for human listeners
- Allow users to customize protection levels
- Evaluate protection strength against real AI models
- Make the tool accessible to musicians, podcasters, journalists, and privacy advocates

---

## 🧰 Tech Stack (In Progress)

**Frontend:**
- JUCE (C++) — Real-time audio processing and cross-platform desktop UI
- React.js — Project website and download portal (planned)

**Backend:**
- Django (Python) — Web integration and API management
- C++ — Audio processing engine (CLI prototype under development)
- RtAudio — Real-time audio stream support

**Design:**
- Figma — Interface prototyping and user flows

---

## 🚧 Current Status: Pre-Alpha

We are in the **very early stages** of development. Work completed or underway:
- 🔬 Research on adversarial attacks against audio models
- ⚙️ CLI-based prototype of the perturbation engine
- 🎨 UI mockups in progress

Next steps:
- Testing against models like Whisper and DeepSpeech
- Build first JUCE desktop prototype
- Implement protection level options
- Launch private Discord-based testing group

---

## 🛠 Planned Features

- 🎚️ **Customizable Protection Levels**
- 🔁 **Real-Time Preview**
- 🧪 **AI Resistance Scoring**
- 🗂️ **Batch Processing of Audio Files**
- 🔌 (Future) VST/AU Plugin Support

---

## 📣 Get Involved

We welcome feedback, collaboration, and testers for our upcoming alpha builds.  
Join the discussion:

- 💬 [Discord Community](https://discord.gg/QdKd8WKG8V)

---

## 📂 Repository Overview

This GitHub organization will host all components of the Dissonance project:

- `pre-aplha` – .wav file parser (metadata and audio data, CLI display)
- `dissonance-core` – Core C++ CLI-based tool that applies adversarial perturbations

---

## 🧑‍🤝‍🧑 Who It's For

- **🎼 Musicians** – Defend your compositions from AI plagiarism.
- **🎧 Podcasters** – Protect your unique voice and content.
- **📰 Journalists** – Prevent AI voice cloning from interviews.
- **🔐 Privacy Advocates** – Control how your voice is used.

---

## 📜 License & Ethics

While the core algorithm will remain closed-source (for protection reasons), we aim to:
- Comply with GDPR, CCPA, and ethical data use standards
- Share research insights and results
- Engage transparently with the open-source and audio communities

---

> "In a world where AI can mimic your voice—make sure it doesn’t *own* it."

---

