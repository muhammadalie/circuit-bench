# Circuit Bench

Build and test electronics circuits virtually before you buy parts: drag parts, wire them, and run real Arduino / ESP32 code (edit and compile it in the page). It shows electron flow, wiring checks, a graph (oscilloscope-style probes and a serial plotter), a virtual phone for Wi-Fi projects, and a parts list with prices.

**Open it:** https://muhammadalie.github.io/circuit-bench/

Every example can run on an **ESP32** (the default) or an **Arduino Uno**: pick the board at the top of Examples ▾, or switch it in the Guide tab. The parts and wires move to the pins the sketch uses on that board (for example the traffic light uses D25/D26/D27 on the ESP32 and 12/11/10 on the Uno).

On a phone, open the link and choose "Add to Home Screen" (iPhone: Share → Add to Home Screen; Android: menu → Install app). It then opens full-screen like an app and works offline. The first Compile & Flash downloads the C++ compiler (about 100 MB) once.

## What is here

- `docs/` is the published app (GitHub Pages serves this folder): `index.html` is the whole app in one file, plus the web-app manifest, icons and the offline service worker.

The app is built from the project's digital-twin sources with `node build-bench.mjs && node build-web.mjs`, which writes `dist/web/`; copy that into `docs/` to publish a new version.

Part drawings: [@wokwi/elements](https://github.com/wokwi/wokwi-elements) (MIT). In-page compiler: [YoWASP Clang](https://yowasp.org/) (loaded from jsDelivr when you first compile).
