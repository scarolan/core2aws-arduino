# Core2 for AWS Arduino Projects

Classic screensavers for the [M5Stack Core2 for AWS](https://docs.m5stack.com/en/core/core2_for_aws), built with PlatformIO and Arduino.

## Screenshots

6 modes that auto-cycle with fade transitions. Tap the screen to skip to the next mode.

| | |
|---|---|
| ![Flying Toasters](screenshots/flying_toasters.png) | ![Pipes](screenshots/pipes.png) |
| **Flying Toasters** -- After Dark homage with animated wing sprites | **Pipes** -- 3D-shaded pipes growing with round elbow joints |
| ![Starfield](screenshots/starfield.png) | ![Matrix Rain](screenshots/matrix_rain.png) |
| **Starfield** -- 500 stars with perspective projection and motion streaks | **Matrix Rain** -- Falling green characters with glowing heads and fade trails |
| ![Mystify](screenshots/mystify.png) | ![DVD Logo](screenshots/dvd_logo.png) |
| **Mystify** -- Bouncing quadrilaterals with color-cycling ghost trails | **DVD Logo** -- The classic bouncing logo, color changes on each edge hit |

## Requirements

- **Hardware:** M5Stack Core2 for AWS (ESP32, 320x240 IPS, 16MB flash)
- **Software:** [PlatformIO](https://platformio.org/) (CLI or VS Code extension)

## Quick Start

Clone the repo, plug in the Core2 for AWS via USB-C, and:

```bash
pio run -t upload
```

To monitor serial output:

```bash
pio device monitor
```

## Controls

- **Tap screen** -- Skip to next mode
- **Auto-cycle** -- Modes transition every 45-90 seconds with a fade-to-black effect
- **NeoPixels** -- The 10 side LEDs glow with colors sampled from the display

## Project Structure

```
src/
  main.cpp              Classic screensavers app
  toaster_sprites.h     Generated toaster/toast sprite data
  dvd_logo.h            Generated DVD logo alpha mask
screenshots/            Screensaver mode captures
platformio.ini          PlatformIO build config
```

## Acknowledgments

This project is built on top of [LovyanGFX](https://github.com/lovyan03/LovyanGFX) by [@lovyan03](https://github.com/lovyan03), which provides the fast graphics engine, sprite system, and display driver. Ported from the [CoreS3 SE version](https://github.com/scarolan/cores3se-arduino).
