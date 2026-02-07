# LinkScope UART Analyzer - User Guide

This document explains how to use LinkScope UART Analyzer step-by-step.

---

## 1. Required Hardware

- ESP32-S3 board
- Target MCU with UART TX
- USB cable
- PC (Windows)

---

## 2. Hardware Connection

| Target Device | ESP32-S3 |
|---------------|----------|
| TX            | GPIO18   |
| GND           | GND      |

Default RX pin: GPIO18

---

## 3. Firmware Setup

1. Open Arduino IDE
2. Open firmware:

firmware/esp32_s3/LinkScope_UART_Analyzer_v0.1.0_esp32_s3.ino

3. Select board: ESP32-S3
4. Select COM port
5. Upload firmware

---

## 4. PC Application Setup

### Option A: Windows EXE (Recommended)

releases/LinkScope_UART_Analyzer_v0.1.0_windows_x64.exe

---

### Option B: Run from Source

pip install pyserial matplotlib
python host/LinkScope_UART_Analyzer_v0.1.0.py

---

## 5. Basic Usage

### Start Capture

B921600
S

### Stop Capture

P

### Clear Screen

C

---

## 6. Command List

S = Start
P = Stop
C = Clear
Bxxxx = Set baud

Example:

B115200
S

---

## 7. Troubleshooting

- Check TX connection
- Check baud rate
- Check COM port
- Replug USB if needed

---

## 8. Recommended Workflow

1. Flash firmware
2. Connect UART
3. Set baud
4. Start capture
5. Analyze data

Happy debugging 🚀
