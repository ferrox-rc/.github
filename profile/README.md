# Welcome to Ferrox-RC 🦀✈️

**Ferrox-RC** is an open-source initiative dedicated to bringing deterministic, memory-safe, `#![no_std]` Rust to radio control hardware and autonomous avionics.

🌐 **Website:** [ferroxrc.com](https://ferroxrc.com)

---

### 🛰️ The Ground-to-Air Ecosystem

- 🎮 **[flysky-i6x-rs](https://github.com/ferrox-rc/flysky-i6x-rs)**: A clean-slate, bare-metal Rust OS for the FlySky FS-i6X transmitter. Sub-4ms packet sync (A7105 / AFHDS 2A), 14-channel matrix mixer, Catmull-Rom spline curves, native 100 Hz USB HID simulator, and >45% free Flash headroom.
- 🎮 **[flysky-i6s-rs](https://github.com/ferrox-rc/flysky-i6s-rs)**: Bare-metal `#![no_std]` Rust transmitter firmware engineered for the FlySky FS-i6S platform, extending deterministic real-time control, mixer pipelines, and modern telemetry to the i6S architecture.
- 🛩️ **[wingfc-rs](https://github.com/ferrox-rc/wingfc-rs)**: Deterministic, high-rate flight controller firmware for sub-250g FPV flying wings and autonomous UAVs on the nRF52840 (Embassy async, 500 Hz control loop, Madgwick AHRS, i-BUS / CRSF telemetry).
- 🛠️ **[wingfc-hardware](https://github.com/ferrox-rc/wingfc-hardware)**: Ultra-compact 25.5×25.5mm hardware carrier board (KiCad schematics & 4-layer PCB layout) hosting the Seeed XIAO nRF52840 Sense, 10 actuator outputs (2 ESCs + 8 servos), integrated DPS310 barometer, and 2S–6S high-efficiency synchronous BEC.

*Built for pilots, makers, and embedded engineers.*
