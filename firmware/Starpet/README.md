# Starpet: A Custom Motion-Controlled Digital Pet

Welcome to the official repository for **Starpet**! This project was built as part of the **Hack Club Half-Life** hardware engineering program.
It was made by looking at the guide "Starbie" published by the Half-Life team. 
It combines a custom-designed Printed Circuit Board (PCB), an ESP32-C3 microcontroller, and an interactive firmware system to create a pocket-sized,
gesture-controlled virtual companion.

---

## Project Overview

Starpet is a 1-bit digital pet that lives inside a 128x64 OLED display. Unlike traditional digital pets,
Starpet doesn't drain its stats while sitting idle on a desk—its attributes only change based on direct user interactions and physical movements tracked
via an onboard accelerometer.

### Meet My Pet
* **Sprite Style:** Custom 32x32 pixel monochrome cat sprite.


---

## Repository Structure

This repository is organized as a unified open-source hardware project:

* `/pcb` — Contains all the KiCad schematics, PCB board layout files, and manufacturing configurations.
* `/firmware` — Houses the Arduino IDE workspace and the core `.ino` execution script.
* `README.md` — This comprehensive documentation manual.
* `LICENSE` — The open-source MIT software license.

---

## Hardware & Pin Configuration

The system runs on a **Seeed Studio XIAO ESP32-C3** development board. Due to the custom routing requirements of my specific PCB layout,
the hardware pins are mapped as follows:

| Component | Schematic Net | ESP32-C3 GPIO | Description |
|--- |--- |--- |--- |
| **OLED & MPU6050 SDA** | SDA Net | **GPIO 7** (D5) | Custom I2C Data Lane |
| **OLED & MPU6050 SCL** | SCL Net | **GPIO 6** (D4) | Custom I2C Clock Pulse |
| **DHT11 Sensor** | DATA Net | **GPIO 3** (D1) | Temperature/Humidity Input |
| **Button 1 (SW1)** | GPIO02 Net | **GPIO 4** (D2) | Radial Menu Open/Confirm |
| **Button 2 (SW2)** | GPIO03 Net | **GPIO 5** (D3) | Stats Display View Toggle |

*Hardware Note: My schematic includes a dedicated 10k pull-up resistor (R1) on the DHT11 DATA line to ensure highly stable climate data streams.*

---

## Gameplay Mechanics & Customs Settings

I customized the core behavioral parameters inside the `BEGINNER SETTINGS` block of the firmware to give my pet a unique personality:

### Starting Stats
When the device boots up, the pet hatches with these starting attribute baselines:
* **Joy:** 80/100
* **Energy:** 80/100
* **Fullness:** 70/100

### The Radial Action Menu
Tilting the board physically activates an "air-mouse" selection ball using the MPU6050 gyroscope. The menu maps four custom options:
1. **TOP: NAP** — Triggers a sleeping animation with floating 'Z' particles.
2. **RIGHT: RUN** — Triggers two high-speed laps across the display.
3. **BOTTOM: JUMP** — Triggers a happy jump.
4. **LEFT: PET** — Triggers hearts floating above the cat.

---

## Software Installation & Dependencies

To compile and upload this firmware locally, the following open-source Arduino libraries are required:
1. **Adafruit GFX Library** — Core graphics drawing functions.
2. **Adafruit SSD1306** — Driver protocol for the 128x64 pixel display screen.
3. **Adafruit MPU6050** — Accelerometer data polling.
4. **DHT sensor library** — Climate module conversion formulas.

---






