# 🤝 Contributing to Dissonance

> Protecting sound, preserving truth.

![CI](https://img.shields.io/badge/ci-passing-brightgreen) ![License](https://img.shields.io/badge/license-MIT-blue) ![Discord](https://img.shields.io/badge/discord-join-blueviolet)

---

## Table of Contents

- [Overview](#overview)
- [Quick Start](#quick-start)
- [How to Contribute](#how-to-contribute)
  - [Code Contributions](#code-contributions)
  - [Pull Request Checklist](#pull-request-checklist)
  - [Issue & Feature Reporting](#issue--feature-reporting)
  - [Research Contributions](#research-contributions)
  - [Design & Documentation](#design--documentation)
- [Development Setup](#development-setup)
- [Code Style & Tests](#code-style--tests)
- [Licensing & Ethics](#licensing--ethics)
- [Need Help?](#need-help)

---

## Overview

Thank you for your interest in contributing to Dissonance — a project focused on protecting human audio from malicious AI usage while preserving sound quality. Contributions from researchers, developers, designers, and creators make this project stronger.

This document explains how to contribute, report issues, request features, and participate in community discussions.

---

## Quick Start

1. Fork the repository
2. Create a branch for your work:

```bash
git checkout -b feature/your-feature-name
```

3. Implement changes and run the project linters/tests locally
4. Push to your fork and open a Pull Request (PR) targeting `main`

---

## How to Contribute

We welcome contributions in many forms. Pick what suits you:

- Code and bug fixes
- Research and evaluation results
- Documentation, design, and translations
- Datasets and reproducible tests (include licensing/consent details)

### Code Contributions

Conventions:

- Branch names: `feature/`, `fix/`, `chore/`
- Keep commits small and focused
- Write clear commit messages, e.g.:

```bash
git commit -m "Add: new perturbation module for audio defense"
```

Before opening a PR, ensure you:

- Run linters and tests
- Add or update tests for new features (where applicable)
- Include a short description and motivation in the PR

### Pull Request Checklist

Please include the following in your PR description:

- [ ] Short summary of the change
- [ ] Motivation and context
- [ ] Screenshots, logs, or sample outputs (if relevant)
- [ ] Links to related issues or research
- [ ] Tests added or updated (where applicable)
- [ ] Passing CI (if available)

PRs that implement research or datasets should also include dataset licenses, consent notes, and reproducible evaluation instructions.

### Issue & Feature Reporting

When opening an issue, include:

- Clear title and concise description
- Steps to reproduce (for bugs)
- Expected vs actual behavior
- Logs, error messages, screenshots, or small repro

We typically tag issues as `bug`, `enhancement`, `research`, or `documentation`.

### Research Contributions

We welcome papers, attack/defense strategies, evaluation code, and datasets. When contributing research:

- Provide reproducible instructions and code
- Include dataset licensing and collection details
- Prefer small, self-contained reproducible examples

If you'd like to collaborate, open a Discussion thread or reach out on Discord.

### Design & Documentation

Non-code contributions are highly valued:

- Improve README and how-tos
- Create visuals and diagrams for the website or README
- Design UI/UX mockups (Figma, etc.)
- Translate or proofread documentation

---

## Development Setup

Below are example commands used in the project (adjust paths to your environment):

Core CLI (C++):

```bash
cd dissonance-core
mkdir -p build && cd build
cmake ..
make
./dissonance input.wav output.wav
```

Web (React / Django):

```bash
cd dissonance-web
npm install
npm run dev
```

If the repo root differs, adapt the paths above to the subproject directories.

---

## Code Style & Tests

- Core: C++17 (JUCE + RtAudio)
- Backend: Python 3.10+
- Frontend: JavaScript (React)
- Formatting: ESLint + Prettier for JS; clang-format for C++

Run these before submitting a PR:

```bash
npm run lint
npm run test
```

Add unit tests for new features and ensure CI passes.

---

## Licensing & Ethics

By contributing you agree that:

- Your contributions comply with the project license
- You respect user privacy and ethical standards
- You will not add code that intentionally harms, surveils, or tracks users

For datasets and human-subjects data, include appropriate consent and license information.

---

## Need Help?

Not sure where to start?

- Join our Discord community
- Open a Discussion in this repo
- Ping a maintainer on the issue or PR

Thank you for helping build Dissonance — your contributions matter.

---

"Protecting sound, preserving truth."
