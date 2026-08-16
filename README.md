# Ocean Board

A custom RP2040 development board.

Ocean Board is a compact, purpose-built devboard around the Raspberry Pi RP2040, designed from scratch rather than bought off the shelf. Built in a single 11-hour session.

## Status

v1 hardware complete — bring-up and firmware in progress

## Features

- **RP2040** microcontroller
- **16MB external QSPI flash** (W25Q128) for extra storage headroom
- **TLV62568 buck converter** for regulated power
- **Dual 16-pin GPIO headers** (left + right) for breakout access
- **BOOTSEL** and **RESET** buttons
- **Micro-USB** for power and programming

## Hardware

| | |
|---|---|
| MCU | RP2040 |
| Flash | W25Q128JVSIQ (16MB) |
| Power regulation | TLV62568ADRLR (buck converter) |
| GPIO | 2x 16-pin headers (`GPIO_LEFT`, `GPIO_RIGHT`) |
| Programming/Power | Micro-USB |
| Controls | BOOTSEL, RESET |

Full bill of materials: [`BOM_RP2040-devboard.csv`](./BOM_RP2040-devboard.csv)

## Getting Started

1. Hold **BOOTSEL** while connecting the board over USB to enter bootloader mode.
2. The board should mount as a USB mass storage device.
3. Drag on a `.uf2` firmware file (e.g. MicroPython or a custom build) to flash it.
4. Press **RESET** to restart the board normally.

## Pinout

_TODO: document the GPIO_LEFT / GPIO_RIGHT header pinout._

## Roadmap

- [ ] Flash and verify basic firmware (blink + USB serial)
- [ ] Load-test the power regulation
- [ ] Document the full pinout
- [ ] Consider a v2 revision (enclosure, more flash, different connector)

## Devlog

Build notes and progress are logged in [`ocean-board-devlog.md`](./ocean-board-devlog.md).

## License

_TODO: pick a license (e.g. MIT, CERN-OHL) for the hardware design and any firmware._
