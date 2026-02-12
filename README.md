# JumpAnalyzer

JumpAnalyzer is a sports performance hardware project designed to measure and analyze vertical jump characteristics using an IMU sensor.

The system captures acceleration and motion data during a jump and calculates:

- Flight time
- Estimated jump height
- Takeoff dynamics
- Landing impact

This repository contains the hardware design (KiCad) and future firmware/software roadmap.

---

# 🏋️ Project Purpose

The goal of JumpAnalyzer is to create a compact wearable device for:

- Basketball players
- Volleyball athletes
- Track & field training
- General athletic performance analysis

The system provides objective performance metrics instead of subjective observation.

---

# 🧠 Measurement Principle

Using an IMU (MPU-9250 or similar):

1. Detect takeoff moment
2. Detect landing moment
3. Calculate flight time (t)
4. Estimate jump height:

h = g * t² / 8

Where:
- g = 9.81 m/s²
- t = flight time

Future versions may include:
- Peak acceleration
- Jump symmetry analysis
- Repetition tracking

---

# 📦 Repository Structure
hardware/kicad/ KiCad schematic and PCB files
hardware/exports/ PDFs, PCB renders, gerbers
hardware/bom/ Bill of Materials
docs/ Concept and algorithm notes
firmware/ (planned) MCU firmware
software/ (planned) data analysis tools
assets/ Images and visual materials# 🔧 Hardware Overview

- IMU: MPU-9250 (9-DOF)
- Interface: I2C or SPI
- Power: 3.3V
- MCU: (planned) ESP32 / STM32
- Form factor: wearable module (shoe-mounted or waist-mounted)

Design focus:
- Small footprint
- Stable power supply
- Noise reduction
- Reliable motion detection

---

# 📊 Planned System Architecture

Sensor → MCU → Filtering → Jump Detection Algorithm → Height Calculation → Data Output

Future:
- Bluetooth transmission
- Mobile app integration
- Data logging (SD card)
- Web dashboard

---

# 🚀 Roadmap

Phase 1:
- Finalize schematic
- PCB routing
- DRC clean
- Generate BOM

Phase 2:
- Firmware to read IMU
- Implement jump detection
- Serial output for debugging

Phase 3:
- Filtering (Kalman / complementary filter)
- Real-time calculation
- Performance metrics

Phase 4:
- Bluetooth data streaming
- Mobile visualization

---

# 📈 Why This Project Matters

Jump performance is a key indicator of:

- Explosiveness
- Power output
- Lower body strength
- Fatigue tracking

JumpAnalyzer aims to provide low-cost hardware alternative to expensive lab systems.

---

# 👨‍💻 Author

Electrical & Electronics Engineering Student  
Embedded Systems & Sports Tech Focus

