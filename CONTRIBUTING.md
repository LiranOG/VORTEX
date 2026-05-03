# Contributing to VORTEX ETERNITY

Thank you for your interest in contributing. This project welcomes improvements across physics, numerics, and visualization.

## Priority Areas

### Physics (High Value)
- **2PN conservative correction** — currently absent from the PN series. The relevant terms are in Blanchet (2014), Living Reviews in Relativity, Section 9.
- **3PN / 3.5PN terms** — would significantly improve accuracy for tight-orbit scenarios
- **Tidal deformability** — relevant for neutron star mergers (GW170817 scenario)
- **Improved QNM fitting** — current ringdown uses leading-order Schwarzschild approximation

### Numerics
- Adaptive timestep control based on local error estimate
- Symplectic integrator option (e.g., Yoshida 4th-order) for long-duration runs
- GPU acceleration via WebGPU (currently CPU-bound)

### Visualization
- Additional scenario presets
- GW polarization animation overlay
- Improved accretion disk shader (GRRT approximation)

## How to Contribute

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/2pn-correction`
3. Make your changes with clear comments referencing source equations
4. Test energy conservation: drift should remain below 0.1% over 10 orbital periods
5. Open a Pull Request with a description of what was changed and why

## Code Style

VORTEX is a single HTML file by design. Keep it that way. All additions go inside `index.html`.

- Comment every non-trivial physics term with the equation number from the source paper
- Use SI units internally, convert for display
- Preserve the existing Hermite-4 integrator structure unless replacing it entirely

## Reporting Issues

Use GitHub Issues for:
- Physics bugs (wrong precession rate, energy non-conservation, etc.)
- Browser compatibility problems
- Scenario initialization errors

Please include: browser version, scenario name, and what behavior you observed vs. expected.

## References

When implementing physics, cite the source equation in a comment:
```javascript
// Peters (1964) Eq. 5.14 — gravitational wave power
const dEdt = -32/5 * G**4/c**5 * m1**2 * m2**2 * (m1+m2) / r**5;
```

---

*VORTEX ETERNITY is a learning and engineering project. Contributions that improve physical accuracy while maintaining browser-native simplicity are especially welcome.*
