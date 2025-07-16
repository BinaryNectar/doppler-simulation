# Doppler Effect Simulation

A 3D web-based simulation demonstrating the Doppler effect using Three.js.

## Overview

This project models an emitter moving through space and emitting spherical wavefronts at a configurable frequency. As the emitter travels, observers perceive a shift in wavelength and frequency, illustrating the Doppler effect in action.

## Demo

Open `index.html` in your browser (preferably via a local HTTP server) to launch the simulation. Use your mouse (click + drag, scroll) to orbit, pan, and zoom with the built‑in `OrbitControls`.

## Features

* **Real‑time WebGL rendering** powered by Three.js
* **Configurable simulation parameters** (velocity, frequency, wavefront count)
* **Interactive camera controls** for exploring the scene
* **Responsive canvas** that adjusts to window resizing

## Prerequisites

* A modern web browser with ES module support
* Internet access (to fetch Three.js and its addons via UNPKG), or serve modules locally
* (Optional) Python 3.x or any simple HTTP server for local hosting

## Installation & Setup

1. **Clone this repository**

   ```bash
   git clone https://github.com/binarynectar/doppler-simulation.git
   cd doppler-simulation
   ```

2. **Start a local server** (recommended to avoid CORS issues):

   ```bash
   python3 -m http.server 8000
   ```

3. **Open the simulation** in your browser:

   ```
   http://localhost:8000/index.html
   ```

## File Structure

```
├── index.html      # Main Doppler simulation entry point
├── second.html     # Alternate version (identical implementation)
└── assets/         # (Optional) folder for local dependencies or assets
```

## Configuration

Inside `index.html`, you can tweak constants near the top of the `<script type="module">` block:

| Constant                 | Description                              |
| ------------------------ | ---------------------------------------- |
| `MAX_WAVEFRONTS`         | Maximum simultaneous wavefronts rendered |
| `VELOCITY_X/Y/Z`         | Emitter velocity components (m/s)        |
| `WAVE_EMISSION_INTERVAL` | Time between emissions (s)               |
| `WAVEFRONT_RADIUS`       | Initial wavefront radius scale           |

Adjust these values to see how they affect the visualization.

## Dependencies

* [Three.js 0.160.0](https://unpkg.com/three@0.160.0/build/three.module.js)
* [OrbitControls addon](https://unpkg.com/three@0.160.0/examples/jsm/controls/OrbitControls.js)
* [es‑module‑shims v1.8.0](https://unpkg.com/es-module-shims@1.8.0/dist/es-module-shims.js)

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/YourFeature`)
3. Commit your changes (`git commit -m "Add YourFeature"`)
4. Push to your branch (`git push origin feature/YourFeature`)
5. Open a Pull Request

## License

This project is released under the [MIT License](LICENSE). Feel free to use, modify, and distribute it.
