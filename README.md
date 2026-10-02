# Jak 3 Jetboard Mechanics Port to Jak 2

<p align="center">
  <img src="https://img.shields.io/badge/OpenGOAL-Mod-blue.svg" alt="OpenGOAL Mod">
  <img src="https://img.shields.io/badge/Game-Jak%202-orange.svg" alt="Game">
  <img src="https://img.shields.io/badge/AI--assisted-Modding-purple.svg" alt="AI Assisted">
</p>

---

> [!NOTE]
> This mod moved from the `jak2/features/jak3-jetBoard` branch of [whozghiar/jak-project](https://github.com/whozghiar/jak-project) to this repository. Earlier releases stay installable from the launcher catalog.

## 📖 Overview
Ports three signature Jetboard mechanics from Jak 3 directly into Jak 2: the Charge / Loaded Jump (`L1` + release `X`), the Circular Zap Attack (`Circle`), and the 180° Quick Turn-Around (`Triangle`) with an exit speed boost, complete with ported animations, particle VFX, and dedicated audio cues.

- **Target Game:** Jak 2
- **Repository:** [`whozghiar/jak2-mod-jak3-jetBoard`](https://github.com/whozghiar/jak2-mod-jak3-jetBoard)

## ✨ Key Features
- **Feature:** **Loaded High Jump:** Hold `L1` (crouch on board) and release `X` to charge kinetic energy and launch Jak into high jumps with charge particles and audio.
- **Feature:** **Circular Zap Attack:** Press `Circle` to unleash a radial electrical sweep with invincibility frames and custom sound effects.
- **Feature:** **180° Quick Turn-Around:** Press `Triangle` to instantly snap 180 degrees and gain a forward speed boost upon exit.

## 🚀 Step-by-Step Guide to Run the Mod

### 1. Select the Active Game
Make sure your environment is targeting Jak 2:
```bash
task set-game-jak2
```

### 2. Binary Compilation
- **Status:** Required (Layer 1 & Layer 2 — Decompiler & Runtime)
- **Details:** Compiles the runtime, compiler, and decompiler required for asset extraction:
```bash
task build-release-game
task build-release-decomp
```

### 3. Asset Extraction
- **Status:** Custom extraction required (Layer 2)
- **Details:** Re-run extraction to process custom assets and modified decompiler configuration:
```bash
task extract
```

### 4. Launch the Game
Run the game natively:
```bash
task boot-game
```
*(Or iterate fast via the OpenGOAL REPL using `task repl`, then hot-reload with `(mi)` and `(r)`).*

### 5. Enable the Mod (OFF by default)
This mod ships **disabled** — a fresh install plays exactly like stock Jak 2.
Press **L3 + SELECT** in-game to open the unified **Mods** menu (works in retail boot, no debug mode required) and go to:

```
Mods ▸ jak3-jetboard ▸ Enable (master)
```

Turning the master toggle ON also arms the three mechanics (`Loaded Jump`,
`Zap Attack`, `Turn-Around`), each of which can then be switched off
individually. Turn the master OFF to fully restore stock jetboard behaviour.

## 🎥 Demonstration Video
[![Demonstration Video](https://img.youtube.com/vi/y-s5oj6Bimo/maxresdefault.jpg)](https://youtu.be/y-s5oj6Bimo)

▶️ **[Watch the demonstration video on YouTube](https://youtu.be/y-s5oj6Bimo)**

## 📖 Technical Documentation
For the complete technical breakdown, architecture, and developer notes, refer to:
- 📄 [`docs/modding/current_mod/jak3-jetboard_readme.md`](docs/modding/current_mod/jak3-jetboard_readme.md)

---
*(AI-assisted)*
