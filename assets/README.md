# VORTEX ETERNITY — Simulation Gallery

All screenshots were captured during live real-time simulation runs at native resolution.
No post-processing was applied. All physical quantities are reported directly from the
Mission Control HUD at the moment of capture.

> **Physics scope note:** VORTEX models pre-merger gravitational dynamics via 2.5PN
> Post-Newtonian radiation reaction. Merger singularities are not resolved — the engine
> is optimized for inspiral, close-encounter, and multi-body orbital evolution.
> Visual explosion effects are cosmetic only and do not represent NR merger physics.

---

## Screenshot Index

---

### `Untitled.jpg` — Stellar Explosion Visual Effect

A manually triggered particle explosion effect demonstrating VORTEX's visual rendering
system. This is a cosmetic feature — the particle field does not represent physically
resolved merger dynamics. The underlying PN integrator continues running during the
effect, and ejecta particles interact gravitationally with surrounding bodies.

**Status:** Visual/cosmetic — not a physically modeled merger event.

---

### `Untitled7.jpg` — EMRI: Extreme Mass-Ratio Inspiral

A Stellar-BH (10M☉) in tight orbit around a Supermassive Black Hole (1000M☉),
capturing the long-duration inspiral phase characteristic of LISA-band sources.

| Parameter | Value |
|-----------|-------|
| **Bodies** | SMBH (1000M☉) + Stellar-BH (10M☉) |
| **Semi-major axis** | a = 113.5 |
| **Eccentricity** | e = 0.321 |
| **Inclination** | i = 0.0° |
| **Orbital period** | T = 127.9 yr |
| **Chirp mass** | M꜀ = 63.0M☉ |
| **Merger timescale** | T_merge = 3.89×10⁷ yr |
| **GW strain h₊** | −1.04×10⁻⁶ G/c⁴ |
| **GW freq** | 1.25×10⁻² Hz_sim |
| **GW phase dephasing** | −1.718 rad |
| **Lense-Thirring spin** | 1.20×10¹, χ_eff = 0.000 |
| **PN parameter X** | 0.0027 |
| **GW Peters quad.** | 4.738×10⁻⁷ c⁵/G |
| **Geometric lapse** | A_min = 0.9973 |
| **Symplectic ΔE** | 2.45×10⁻⁵ |
| **Peak velocity** | 6314.8 km/s |
| **Min separation** | 98.2 |

The rosette orbital pattern visible around the BH is a consequence of relativistic
periapsis precession — a direct 1PN effect on the inspiral trajectory.

---

### `VORTEX_1.jpg` — N-body Cascade: 7-Body Tri-Species System

A complex multi-body scenario featuring 7 objects of mixed astrophysical type
undergoing a gravitational cascade — Phase III of a multi-stage encounter sequence.

| Parameter | Value |
|-----------|-------|
| **Bodies** | 7 (mixed: R136a1-class stars + compact objects) |
| **Phase** | III — CASCADE (1M/0T) |
| **Simulation time** | T = 134.55 yr |
| **Peak velocity** | 5954.1 km/s |
| **KE** | 7.501×10⁴¹ |
| **PE** | −1.191×10⁴² |
| **Hamiltonian H(Q,P)** | −4.409×10⁴¹ |
| **Angular momentum** | 2.41×10⁵ |
| **Geometric lapse** | A_min = 0.9966 |
| **Symplectic ΔE** | 3.12×10⁻⁵ |
| **GW Peters quad.** | 3.170×10⁻² c⁵/G |
| **GW Mass Defect** | 0.006M☉ |
| **GW phase dephasing** | 3.958 rad |
| **FPS / SUB** | 60 / 10 |

The minimap (lower-left) shows the full system extent with all 7 bodies tracked.
Mission Control displays real-time Kahan-compensated Hamiltonian, confirming
energy conservation across the cascade.

---

### `Untitled3.jpg` — ZKL Triple: Kozai-Lidov Hierarchical System

A three-body hierarchical system demonstrating the Kozai-Lidov mechanism —
periodic eccentricity oscillations driven by the outer disturber's gravitational
torque on the inner binary. Rendered in cinematic mode (no HUD) for visual clarity.

| Parameter | Value |
|-----------|-------|
| **Bodies** | KL-Star-A (200M☉) + KL-Star-B (180M☉) + KL-Disturber (800M☉) |
| **Inner binary semi-major axis** | a = 42.5 |
| **Inner binary eccentricity** | e = 0.413 |
| **Inclination** | i = 0.1° |
| **Inner orbital period** | T = 47.7 yr |
| **Chirp mass** | M꜀ = 165.1M☉ |
| **Merger timescale** | T_merge = 3.69×10⁵ yr |
| **GW strain h₊** | 3.09×10⁻⁴ G/c⁴ |
| **GW strain h×** | 9.82×10⁻⁶ G/c⁴ |
| **GW dominant freq** | 6.13×10⁻² Hz_sim |
| **Lense-Thirring spin** | 1.96×10³, χ_eff = −0.072 |
| **GW phase dephasing** | 0.052 rad |

The orbital trails show the inner binary inspiral trajectory under the KL
eccentricity oscillation cycle. The massive disturber (800M☉) visible upper-left
drives the secular perturbation that pumps the inner eccentricity.

---

### `Untitled6.jpg` — Gravitational Infall: 5-Body with GW Diagnostics

A 5-body system in Phase I (Gravitational Infall), captured during the early
approach phase with full GW diagnostics active — chirp mass, Lense-Thirring
precession, and quadrupole strain computed live.

| Parameter | Value |
|-----------|-------|
| **Bodies** | 5 |
| **Phase** | I — GRAVITATIONAL INFALL |
| **Simulation time** | T = 2025.68 yr |
| **Chirp mass** | M꜀ = 4.2M☉ |
| **Merger timescale** | T_merge = 1.41×10¹⁰ yr |
| **Eccentricity** | e = 0.004 |
| **GW strain h₊** | 1.04×10⁻⁷ G/c⁴ |
| **Angular momentum \|L\|** | 1.27×10³ |
| **Linear momentum \|P\|** | 4.64 |
| **Lense-Thirring spin** | 7.21×10², χ_eff = −0.128 |
| **GW Peters quad.** | 3.070×10⁻¹¹ c⁵/G |
| **Geometric lapse** | A_min = 0.9986 |
| **Symplectic ΔE** | 1.59×10⁻⁷ |
| **PN parameter X** | 0.0014 |
| **GW phase dephasing** | 0.016 rad |
| **FPS / SUB** | 60 / 100 |

The extremely low ΔE = 1.59×10⁻⁷ and SUB=100 confirm high-precision integration
during this early-phase encounter. The nearly circular orbit (e=0.004) and long
merger timescale place this system in the quasi-circular Peters regime.

---

### `VORTEX_2.png` — Oort Cloud Infall: Host-Star + 8-Comet System

A 9-body system consisting of a massive host star (300M☉) surrounded by 8 cometary
bodies in highly eccentric, inclined orbits — simulating a long-period gravitational
infall scenario analogous to an Oort Cloud or outer debris disk encounter.

| Parameter | Value |
|-----------|-------|
| **Bodies** | Host-Star (300M☉) + Comet-1 through Comet-8 (PLANET-class) |
| **Phase** | I — GRAVITATIONAL INFALL |
| **Simulation time** | T = 21332.80 yr |
| **Temporal flow** | 1000.0× |
| **FPS / SUB** | 60 / 200 |
| **Dominant binary semi-major axis** | a = 412.8 |
| **Dominant binary eccentricity** | e = 0.889 |
| **Inclination** | i = 26.1° |
| **Orbital period** | T = 1626.1 yr |
| **Chirp mass** | M꜀ = 0.2M☉ |
| **Merger timescale** | T_merge = 1.70×10¹² yr |
| **GW strain h₊** | −1.66×10⁻¹⁰ G/c⁴ |
| **GW strain h×** | 1.41×10⁻¹¹ G/c⁴ |
| **GW dominant freq** | 4.74×10⁻⁴ Hz_sim |
| **KE** | 5.704×10³⁴ |
| **PE** | −1.135×10³⁶ |
| **Hamiltonian H(Q,P)** | −1.078×10³⁶ |
| **Peak velocity** | 420.3 km/s |
| **Min separation** | 527.6 |
| **Angular momentum \|L\|** | 2.14 |
| **Linear momentum \|P\|** | 2.22×10⁻⁴ |
| **Lense-Thirring spin** | 3.60×10², χ_eff = −0.103 |
| **GW Peters quad.** | 1.349×10⁻¹⁶ c⁵/G |
| **PN parameter X** | 0.0002 |
| **GW phase dephasing** | −1.604 rad |
| **Geometric lapse** | A_min = 0.9998 |
| **Symplectic ΔE** | 8.44×10⁻¹⁰ |

The exceptionally low ΔE = 8.44×10⁻¹⁰ at SUB=200 represents the highest-precision
integration in this gallery — a consequence of the wide separations and low PN
parameter (X=0.0002) in this long-period system. The near-unity lapse (0.9998)
confirms negligible relativistic corrections at these orbital scales.
The extreme merger timescale (1.70×10¹² yr) confirms this is a purely Newtonian-regime
gravitational infall with negligible GW-driven inspiral.

---

### `VORTEX_3.jpg` — GW150914: First Detected Binary Black Hole Merger

A faithful recreation of the GW150914 event — the first gravitational wave detection
by LIGO (2015) — using the exact component masses reported in the discovery paper.
Captured during Phase II (Close Encounter) with the spacetime grid deformation and
accretion disk geometry visible in real time.

| Parameter | Value |
|-----------|-------|
| **Bodies** | BH-36 (36M☉) + BH-29 (29M☉) |
| **Phase** | II — CLOSE ENCOUNTER |
| **Simulation time** | T = 662.37 yr |
| **Semi-major axis** | a = 60.2 |
| **Eccentricity** | e = 0.003 |
| **Inclination** | i = 14.0° |
| **Orbital period** | T_orb = 194.5 yr |
| **Chirp mass** | M꜀ = 28.1M☉ |
| **Merger timescale** | T_merge = 8.81×10⁸ yr |
| **GW strain h₊** | −2.23×10⁻⁶ G/c⁴ |
| **GW strain h×** | 3.04×10⁻⁷ G/c⁴ |
| **GW dominant freq** | 1.03×10⁻² Hz_sim |
| **Lense-Thirring spin** | 2.46×10¹, χ_eff = 0.161 |
| **GW Peters quad.** | 8.749×10⁻⁹ c⁵/G |
| **PN parameter X** | 0.0004 |
| **GW phase dephasing** | 0.000 rad |
| **KE** | 3.019×10³⁹ |
| **PE** | −6.054×10³⁹ |
| **Hamiltonian H(Q,P)** | −3.035×10³⁹ |
| **Peak velocity** | 1073.0 km/s |
| **Min separation** | 60.3 |
| **Angular momentum \|L\|** | 1.88×10³ |
| **Linear momentum \|P\|** | 7.30×10⁻² |
| **Geometric lapse** | A_min = 0.9998 |
| **Symplectic ΔE** | 5.28×10⁻⁹ |
| **FPS / SUB** | 60 / 10 |

The near-circular orbit (e=0.003) and low PN parameter (X=0.0004) place this system
in the quasi-circular inspiral regime consistent with the original LIGO parameter
estimation. The χ_eff = 0.161 reflects the aligned-spin contribution to the orbital
evolution. The spacetime grid deformation visible in the image is driven by the
combined 65M☉ of the binary at close encounter.

---

*All simulations run in real time at 60 FPS using a 4th-order Hermite predictor-corrector
integrator with Kahan compensated summation. PN dynamics implemented through 2.5PN order.*
