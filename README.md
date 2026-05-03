<div align="center">

# VORTEX ETERNITY

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue?style=flat&logo=github)](https://liranog.github.io/VORTEX/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Physics](https://img.shields.io/badge/Physics-2.5PN%20Post--Newtonian-purple?style=flat)]()

[![Language](https://img.shields.io/badge/Language-JavaScript-F7DF1E?style=flat&logo=javascript)](https://github.com/LiranOG/VORTEX)
[![Three.js](https://img.shields.io/badge/Three.js-r128-black?style=flat&logo=three.js)](https://threejs.org/)

 **Interactive relativistic gravitational dynamics — running entirely in your browser.**

VORTEX ETERNITY is a single-file HTML/JavaScript application that makes relativistic gravitational physics interactive and inspectable in real time. It implements Post-Newtonian dynamics up to 2.5PN order, full gravitational-wave emission, and a suite of astrophysical preset scenarios — all rendered live with Three.js/WebGL.

---

</div>

## 🌐 Live Demo

**[→ Launch VORTEX ETERNITY](https://liranog.github.io/VORTEX/)**

>**No installation. No dependencies to install. Open in any modern browser.**

---

## 📖 Extended Technical Documentation

This repository contains the standalone deployment of VORTEX ETERNITY.
A deeper technical README — covering the full architecture, zero-allocation
hot-path design, cinematic recording system, Tactical Minimap 3.0, and the
complete keyboard reference — is maintained inside the GRANITE-NR ecosystem:

**[→ VORTEX ETERNITY — Full Technical Documentation](https://github.com/LiranOG/Granite-NR/tree/main/viz/vortex_eternity)**

VORTEX serves as the interactive WebGL frontend for the GRANITE numerical
relativity engine, and its extended docs reflect that tighter integration
with the broader simulation ecosystem.

---

## ✨ Features

### Physics Engine
- **Hermite-4 integrator** with Kahan summation for energy stability
- **Post-Newtonian dynamics through 2.5PN** (radiation reaction / gravitational-wave back-reaction)
- **Rodrigues-formula spin precession** — geodetic and frame-dragging contributions
- **Kerr ISCO calculation** — innermost stable circular orbit for spinning black holes
- **Quasi-normal mode (QNM) ringdown** — frequency and damping time from remnant parameters
- **Gravitational-wave recoil kick** — asymmetric mass ejection velocity using the Campanelli formula
- **Solar System initialization from J2000.0 state vectors** — planets placed at physically correct positions

### Gravitational Wave Diagnostics
- Real-time GW strain (h₊, h×) computation via Peters quadrupole formula
- Live chirp frequency and energy/momentum loss tracking
- Accretion disk luminosity rendering (Novikov-Thorne model)
- CSV telemetry export for offline analysis

### Astrophysical Scenarios
| Scenario | Description |
|----------|-------------|
| **GW150914** | First detected binary black hole merger (LIGO 2015) |
| **GW170817** | Binary neutron star merger with kilonova |
| **EMRI** | Extreme mass-ratio inspiral — stellar black hole orbiting SMBH |
| **ZKL Triple** | Kozai-Lidov oscillations in a hierarchical triple system |
| **Galactic Center** | S-star cluster orbiting Sgr A* |

### Visualization
- Three.js-based 3D rendering with tactical minimap and HUD
- Real-time orbit trail rendering with fade
- Gravitational lensing approximation overlay
- Accretion disk geometry with Doppler color-shift

---

## 🛠 Technical Implementation

### Architecture
VORTEX ETERNITY is deliberately a **single self-contained HTML file**. This was a deliberate design constraint: zero build tooling, zero dependency management, instant deployment anywhere.

### Numerical Methods
The integrator uses a **4th-order Hermite predictor-corrector** scheme, which is standard in N-body astrophysics for its energy conservation properties. Kahan compensated summation is applied to accumulated forces to suppress floating-point drift over long integrations.

The Post-Newtonian expansion is implemented through **2.5PN order**, covering:
- **0PN** — Newtonian gravity
- **1PN** — Special-relativistic corrections (periapsis precession)
- **1.5PN** — Gravitomagnetic / spin-orbit coupling
- **2PN** — Conservative relativistic corrections  
- **2.5PN** — Radiation reaction (gravitational-wave energy loss)

> **Known open issue:** The 2PN conservative correction term is currently absent from the PN series — a gap identified during development and planned for a future revision. Energy drift remains below ~0.01% on the standard scenarios.

### Spin Dynamics
Spin precession is computed using the **Rodrigues rotation formula** applied per timestep, accumulating the geodetic (de Sitter) and frame-dragging (Lense-Thirring) contributions. This avoids gimbal lock while remaining computationally lightweight for real-time use.

---

## 🚀 Usage

### Run Locally
```bash
git clone https://github.com/LiranOG/VORTEX-ETERNITY.git
cd VORTEX-ETERNITY
# Open index.html in any modern browser
open index.html
```

No build step. No npm install. Just open the file.

### Controls
| Input | Action |
|-------|--------|
| Left drag | Rotate camera |
| Scroll | Zoom |
| Right drag | Pan |
| Scenario buttons | Load preset |
| CSV Export | Download telemetry |

---

## 📊 Telemetry Export

VORTEX exports real-time simulation data as CSV, including:
- Timestep, simulation time
- Per-body: position (x,y,z), velocity (vx,vy,vz), mass, spin
- GW strain (h₊, h×), chirp frequency
- Total energy, angular momentum, energy drift %

This allows offline analysis with Python/NumPy or any data tool.

---

## 🔭 Development Methodology

VORTEX ETERNITY was developed through **AI-orchestrated implementation** — directing model-generated code against published formulae (Peters 1964, Blanchet 2014, Campanelli 2007), then auditing, integrating, and verifying numerical behavior.

This is an engineering and learning project rather than credentialed research. Its value lies in hands-on intuition for relativistic two-body dynamics and the practical challenges of real-time scientific visualization.

---

## 📚 References

- Peters, P.C. (1964). *Gravitational Radiation and the Motion of Two Point Masses*. Physical Review.
- Blanchet, L. (2014). *Gravitational Radiation from Post-Newtonian Sources*. Living Reviews in Relativity.
- Campanelli, M. et al. (2007). *Maximum Gravitational Recoil*. Physical Review Letters.
- Buonanno, A. & Damour, T. (1999). *Transition from inspiral to plunge in binary black hole coalescences*. Physical Review D.

---

## 🤝 Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

Pull requests are welcome, particularly for:
- The missing 2PN conservative correction
- Additional PN orders (3PN, 3.5PN)
- Additional astrophysical scenarios
- Performance optimizations for the integrator

---

## 📄 License

MIT License — see [LICENSE](LICENSE) for details.

---

## 👤 Author

**Liran Schwartz** · [LinkedIn](https://linkedin.com/in/liran-schwartz) · [ORCID](https://orcid.org/0009-0008-8035-1308) · [GitHub](https://github.com/LiranOG)

*Part of an ongoing independent research program in computational physics and AI systems.*
