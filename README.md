# Project README

## Summary
Minimal C\+\+ Arduino project that initializes an SSD1306 128x64 OLED over I2C and prints status text. The main sketch and sources are in `src`.

## IDE
- IDE: `CLion`
- IDE version: `CLion 2025.3.2`

## Code overview
- Main sketch: `src/main.cpp`
- Initializes Serial at `115200` baud.
- Initializes SSD1306 OLED at I2C address `0x3C`.
- Displays static text on the OLED; `loop()` is a placeholder for user code.

## Libraries
- `Wire` — I2C library (Arduino core)
- `Adafruit_GFX` — graphics primitives
- `Adafruit_SSD1306` — SSD1306 OLED driver

## Dependencies
- Arduino core for the target board (e.g., `arduino:avr` or `arduino:samd` depending on board)
- Arduino CLI or PlatformIO (or a CMake-based Arduino toolchain) integrated into `CLion`
- Library versions (example):
  - `Adafruit GFX` >= 1.11.0
  - `Adafruit SSD1306` >= 2.5.7
- USB driver for your board (Windows)

## Components (used with OLED)
- SSD1306 128x64 OLED display (I2C, address `0x3C`)
- Microcontroller board (example: `Arduino UNO R4`)
- USB cable for power and programming
- Optional: logic-level shifter (if voltage levels differ), female-to-male jumper wires, breadboard

## Wiring (I2C OLED)
- Connect `VCC` to `5V` or `3.3V` (match OLED module requirements)
- Connect `GND` to `GND`
- Connect `SDA` to board SDA pin (e.g., A4 on some AVR boards)
- Connect `SCL` to board SCL pin (e.g., A5 on some AVR boards)
- Ensure pull-up resistors are present on SDA/SCL (many modules include them)

## Software requirements
- Operating system: `Windows` (development)
- `CLion 2025.3.2`
- Arduino CLI or PlatformIO (installed and configured)
- Board support package for your board (installed via Arduino CLI or PlatformIO)
- Serial monitor (CLion plugin, Arduino CLI `monitor`, or external tool like PuTTY)

## Hardware requirements
- `Arduino UNO R4` (or compatible board)
- SSD1306 128x64 I2C OLED module (`0x3C`)
- USB cable, wires, optional breadboard

## Build & run (short)
1. Open `CLion` and open the project root.
2. Configure toolchain: set up Arduino CLI / PlatformIO integration or a CMake Arduino toolchain.
3. Install required libraries (`Adafruit_GFX`, `Adafruit_SSD1306`) via PlatformIO, Arduino Library Manager, or copy into project `lib`.
4. Select target board and COM port.
5. Build and upload from CLion run configuration or use Arduino CLI: `arduino-cli compile --fqbn <board> && arduino-cli upload -p <COM> --fqbn <board>`
6. Open serial monitor at `115200` baud to view logs.

## Files of interest
- `src/main.cpp` — main sketch
- `CMakeLists.txt` (if present) — build settings / integration

## Author
- `charvi1405` (GitHub)

## License
Specify preferred license (e.g., MIT) or remove this section.
