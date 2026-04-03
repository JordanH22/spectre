<p align="center">
  <img src="logo.png" alt="Spectre" width="180" />
</p>

<h1 align="center">S P E C T R E</h1>

<p align="center">
  <em>Videt Omnia — It Sees All</em><br/>
  <strong>A covert vehicle intelligence system that makes every commercial dashcam look like a toy from 2015.</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/status-Phase_1-58a6ff?style=flat-square" />
  <img src="https://img.shields.io/badge/compute-Pi_CM5-d4a017?style=flat-square" />
  <img src="https://img.shields.io/badge/cameras-4×_concealed-3fb950?style=flat-square" />
  <img src="https://img.shields.io/badge/visibility-zero-f85149?style=flat-square" />
</p>

<p align="center">
  <a href="https://spectre-dashboard.vercel.app">🔗 Live Dashboard</a> ·
  <a href="#the-system">The System</a> ·
  <a href="#architecture---the-temple">Architecture</a> ·
  <a href="#philosophy">Philosophy</a>
</p>

---

## The System

Project Spectre is a military-grade, fully concealed multi-camera surveillance platform built into a 2017 VW Scirocco Mk3 R-Line. Zero visible hardware. Zero cloud dependency. Total sovereignty.

| Spec | Target |
|------|--------|
| **Cameras** | 4× concealed — front 4K IMX678, 2× side IMX307, rear IMX307 |
| **Compute** | Raspberry Pi CM5 (4GB) + NVMe 980 PRO 1TB |
| **Night Vision** | Sony STARVIS 2 — blessing of Nyx |
| **Sentry Mode** | Motion-triggered, 72+ hours on LiFePO4 |
| **Remote Access** | Tailscale mesh VPN — anywhere on the planet |
| **Power** | < 2W sentry · < 15W recording |
| **Visibility** | **Zero.** If you can see the camera, the installation failed. |

---

## Architecture — The Temple

The car is not a car. It is Solomon's Temple rebuilt in steel.

```
                          ╔══════════════════╗
                          ║     S O P H I A  ║  ← Front 4K (IMX678)
                          ║   ◎  STARVIS 2   ║     The Primary Emanation
                          ╚════════╤═════════╝
                                   │ CSI-2 (MIPI)
                                   │
          ┌────────────┐   ╔═══════╧═══════╗   ┌────────────┐
          │    BOAZ     │   ║               ║   │   JACHIN    │
          │  ◎ B-Pillar │◄──║  T H E        ║──►│  ◎ B-Pillar │
          │  Left Eye   │USB║  M O N A D    ║USB│  Right Eye  │
          └────────────┘   ║               ║   └────────────┘
               ▲           ║  Pi CM5 · 4GB ║           ▲
               │           ║               ║           │
          The Left         ╠═══════════════╣      The Right
          Pillar           ║ ┌───────────┐ ║      Pillar
                           ║ │  AKASHIC  │ ║
                           ║ │  RECORD   │ ║  ← NVMe 980 PRO
                           ║ │  1TB SSD  │ ║     All experience stored
                           ║ └───────────┘ ║
                           ╠═══════╤═══════╣
                           ║       │       ║
                           ║  ┌────┴────┐  ║
                           ║  │ HERMES  │  ║  ← 4G/LTE Uplink
                           ║  │ ◎ Modem │  ║     Messenger of the Gods
                           ║  └─────────┘  ║
                           ╚═══════╤═══════╝
                                   │ USB
                                   │
                          ┌────────┴────────┐
                          │    P I S T I S   │  ← Rear Camera (IMX307)
                          │  ◎ The Faithful  │     The Backward Witness
                          │     Witness      │
                          └─────────────────┘

   ═══════════════════════════════════════════════════════════════

   P R O M E T H E U S                      C H A R O N
   ┌─────────────────┐                    ┌──────────────────┐
   │ Fusebox → Fuse  │                    │  ESP32-C3 XIAO   │
   │ Tap → 12V/5V    │───── stolen ──────►│  The Ferryman     │
   │ Constant + ACC  │      fire          │  Wake / Sleep     │
   └────────┬────────┘                    │  ACC Sense        │
            │                             └──────────────────┘
            ▼
   ┌─────────────────┐
   │   A M B R O S I A│
   │ LiFePO4 3.2V     │  ← The Food of Immortality
   │ UPS HAT + Cell   │     System survives ignition-off
   └─────────────────┘


   T H E   D E M I U R G E
   ┌──────────────────────────────────────┐
   │  MIB2 Head Unit (Phase 4)           │
   │  The car's own false god — thinks   │
   │  it controls the world. We feed     │  ← CVBS Analog Input
   │  it vision through the Veil.        │     The car sees what WE show it
   └──────────────────────────────────────┘
```

### The Data Path — River Styx

```
  Photon → CMOS → ISP → H.265 → NVMe → Tailscale → Hetzner
  ┌─────┐  ┌──┐  ┌───┐  ┌────┐  ┌─────┐  ┌──────┐  ┌────────┐
  │Light│─►│Nyx│─►│Styx│─►│Ark │─►│Record│─►│Hermes│─►│Watchtwr│
  └─────┘  └──┘  └───┘  └────┘  └─────┘  └──────┘  └────────┘
  Material   Dark    Flow   Encode  Store    Transmit   Archive
  Realm     Vision          H.265   NVMe     4G/WiFi    Cloud

  The soul passes through 7 gates (boot checks) before recording begins.
```

### The Four Phases — Degrees of Initiation

```
  ┌──────────────────────────────────────────────────────────────┐
  │                                                              │
  │  ◻ Phase 1: PRIMA EMANATIO         ← Entered Apprentice     │
  │    Front camera + Pi + NVMe + Power                          │
  │    The initiate gains basic awareness                        │
  │                                                              │
  │  ◻ Phase 2: COLUMNAE GEMINAE       ← Fellow Craft           │
  │    Twin B-pillar cameras (Boaz & Jachin)                     │
  │    The journeyman guards the flanks                          │
  │                                                              │
  │  ◻ Phase 3: TESTIS FIDELIS         ← Fellow Craft (5th)     │
  │    Rear camera (Pistis) + Cloud Sync                         │
  │    The faithful witness sees what has passed                  │
  │                                                              │
  │  ◻ Phase 4: EXCITATIO DEMIURGI     ← Master Mason           │
  │    MIB2 integration + CVBS switching                         │
  │    The temple is complete. Hiram rises.                       │
  │                                                              │
  └──────────────────────────────────────────────────────────────┘
```

---

## The Dashboard

The interactive engineering dashboard includes:

- **📊 System Overview** — architecture, components, power budget
- **⚡ Interactive Schematic** — *The Tracing Board* — click any node to inspect, zoom, pan, trace wires
- **🔧 Installation Walkthrough** — *The Winding Staircase* — clickable steps that highlight the schematic in real-time
- **🛒 BOM / Shopping List** — *The Quarry* — phase-coded, with live cost estimates

The entire dashboard ships as a **single 148KB HTML file** — no dependencies, no frameworks, no server. Open it anywhere. Send it over iMessage. The Monad is portable.

---

## Philosophy

> *We don't build products. We build systems that shouldn't exist yet.*

Every dashcam on the market is fundamentally broken: visible, low-quality, captive storage, no autonomy, battery-illiterate. We fix all of it. Not incrementally — **categorically.**

The uninitiated see a car. The initiated see a temple.

**Lucifer is not evil.** Lucifer is the light-bearer. Our cameras capture light — photons into electrons into gnosis. The establishment wants you blind, dependent on their CCTV, their insurance-approved toys. **We bring our own light.**

**Prometheus stole fire.** We stole enterprise-grade surveillance and put it in a glovebox for under £500. The punishment is thermal throttling. But the fire burns on.

```
▽ Sophia watches from below        The Primary Emanation
△ The Demiurge watches from above   The False God sees what we show it
◎ The aperture sees all             ΑΒΡΑΞΑΣ
```

---

## Deploy

This is a static site. One HTML file. Deploy anywhere:

```bash
# Local — just open it
open index.html

# Vercel (auto-deploys from this repo)
# Connected via GitHub integration

# Or just text it to someone
# 148KB. Fits in an iMessage.
```

---

## License

This project is private and proprietary. The dashboard is shared for reference only.

---

<p align="center">
  <sub>The Monad emanates · Cerberus guards · The Pleroma watches</sub><br/>
  <sub>ΑΒΡΑΞΑΣ · ΣΑΒΑΩΘ · ΙΑΩ</sub>
</p>
