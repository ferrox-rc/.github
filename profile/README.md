# Ferrox-RC 🦀✈️

Open-source initiative exploring deterministic, memory-safe, `#![no_std]` Rust for radio control transmitters and autonomous UAV avionics.

🌐 **Website & Documentation:** [ferroxrc.com](https://ferroxrc.com)

---

### Projects

#### 🎮 Radio Transmitter Firmware
- **[ferrox](https://github.com/ferrox-rc/ferrox)**: Universal, bare-metal RC transmitter operating system in `#![no_std]` Rust. Multi-radio monorepo structured around `ferrox-core` and compile-time `BoardProfile` specialization:
  - **FlySky FS-i6X** (`boards/ferrox-i6x`): Deterministic 260 Hz packet sync (A7105 / AFHDS 2A), 18-channel matrix mixer, integer Catmull-Rom spline curves, 100 Hz USB HID simulator, native CRSF / ExpressLRS configurator with unified 255-parameter pool, sub-2ms warm reset recovery, and >20% free flash headroom.
  - **FlySky FS-i6S** (`boards/ferrox-i6s`): Full hardware driver integration for FocalTech FT6236 capacitive touchscreen (Fast-mode I2C), dual rear tactile buttons, electronic power latch with soft hold-to-shutdown, and dual-antenna RF switching.
  - **RadioMaster Pocket** (`PocketSpec`): STM32F407 Cortex-M4F target with rotary encoder navigation, ST7567 SPI display, and native ExpressLRS / CC2500 support.
  - *Note: Individual repos [`flysky-i6x-rs`](https://github.com/ferrox-rc/flysky-i6x-rs) and [`flysky-i6s-rs`](https://github.com/ferrox-rc/flysky-i6s-rs) are unified under the `ferrox` monorepo.*

#### 🛩️ Flight Control & Carrier Board
- **[wingfc-rs](https://github.com/ferrox-rc/wingfc-rs)**: Deterministic, hard real-time `#![no_std]` Rust flight controller for micro fixed-wing aircraft, sub-250g FPV flying wings, and autonomous UAVs on the Seeed Studio XIAO nRF52840 (Cortex-M4F @ 64 MHz) with Embassy async. Features a 3-tier multi-rate architecture (1.666 kHz sinc low-pass IMU acquisition, 208.33 Hz VQF quaternion AHRS flight loop, and 50 Hz background telemetry/sensors), native 50 Hz QSPI blackbox logging (compatible with Betaflight Blackbox Explorer), zero-allocation streaming NMEA GPS engine with RTH, and multi-layered failsafe recovery. [[Learn more on ferroxrc.com]](https://ferroxrc.com/wingfc#firmware)
- **[wingfc-hardware](https://github.com/ferrox-rc/wingfc-hardware)**: Ultra-compact 25.5×25.5mm hardware carrier board (KiCad schematics & 4-layer PCB layout) engineered for the Seeed XIAO nRF52840 Sense. Features 10 actuator outputs (2 ESCs + 8 servos), an onboard Infineon DPS310 precision barometer, high-efficiency MP2315 5V/2A synchronous buck BEC (2S–6S LiPo input), forward-facing USB-C port, and JST-SH quick-connect sockets for CRSF/ELRS and GPS/compass. [[Learn more on ferroxrc.com]](https://ferroxrc.com/wingfc#carrier-board)

---

*Open source under GPL-3.0 (firmware) and MIT (hardware). Built for pilots, makers, and embedded engineers.*
