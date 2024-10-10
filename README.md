# Zap Net: Interactive Wi-Fi Deauther (V2)

![zapnet](https://github.com/user-attachments/assets/68302b5b-5810-4cdd-86bd-e1deba22d1ff)

## Overview

**Zap Net** is an Open Source Wi-Fi Deauther project designed for ethical hacking, penetration testing, and educational purposes. This tool allows you to:

- **Scan Networks**: Identify nearby Wi-Fi networks.
- **Deauthenticate Users**: Disconnect devices from a Wi-Fi network.
- **Create Fake Access Points**: Clone multiple networks to confuse users.

The goal of this project is to provide cybersecurity enthusiasts, students, and professionals with an easy-to-use tool for learning about wireless network vulnerabilities and testing security measures.

---

## Table of Contents

1. [Project Description](#description)
2. [Pre-requisites](#pre-requisites)
3. [Assembly Instructions](#assembly)
4. [Software Installation](#software)
5. [Usage](#usage)
6. [Disclaimer](#disclaimer)

---

<a name="description"></a>

## 1. Project Description

**Zap Net** is built on the WeMos D1 Mini ESP8266 platform and uses a simple OLED display for user interaction. The device works by sending deauthentication frames to disconnect devices from a Wi-Fi network and can also create multiple fake networks to demonstrate security vulnerabilities. 

> **Note**: This project is for educational purposes only and should not be used for any malicious activities. 

---

<a name="pre-requisites"></a>

## 2. Pre-requisites
![zapnet_kit](https://github.com/user-attachments/assets/d019a502-98fd-4009-b9da-c31b0a989dd1)

To build your own **Zap Net**, you will need the following components:

### Hardware:
- **Zap Net Breadboard**: Custom PCB designed for this project.
- **WeMos D1 Mini (ESP8266)**: Microcontroller board.
- **SH1106 1.3 inch OLED display** (128x64 pixels): User interface.
- **3 Tactile Push Buttons**: For navigating the interface.
- **Soldering Iron and Lead**: For assembling the device.

### Software:
- **Arduino IDE**: For flashing the firmware.

---

<a name="assembly"></a>

## 3. Assembly Instructions

Follow these steps to assemble the hardware:

### Step 1: Solder the OLED Display
- Line up the OLED display to the holes on the PCB.
- Push it in and solder it to the board.

### Step 2: Solder the Header Pins to the WeMos D1 Mini
- Carefully solder the header pins to the WeMos D1 Mini for proper alignment.

### Step 3: Attach the WeMos D1 Mini to the PCB
- Solder the WeMos D1 Mini to the PCB, ensuring the pins match the labels on the board.

---

<a name="software"></a>

## 4. Software Installation

Follow these instructions to set up the firmware on your **Zap Net** device:

### Step 1: Install Arduino IDE
- Download and install the latest version of Arduino IDE from [here](https://www.arduino.cc/en/software).

### Step 2: Add Board Manager URL
- Open Arduino IDE.
- Go to **Preferences** (`Ctrl+Comma` or File -> Preferences).
- In the **Additional Boards Manager URLs** field, add the following URL:
  ```
  https://raw.githubusercontent.com/SpacehuhnTech/arduino/main/package_spacehuhn_index.json
  ```

### Step 3: Install Deauther Board
- Open the **Boards Manager** (Tools -> Board -> Boards Manager).
- Search for `Deauther ESP8266 Boards` and install it.

### Step 4: Configure the Board Settings
- In Arduino IDE, go to **Tools** -> **Board** -> **Deauther ESP8266 Boards** -> Select **Dstike Deauther**.
- Set the following parameters in **Tools**:
  - **Upload Speed**: `921600`
  - **Deauther Config**: `DSTIKE Deauther OLED V2`
  - **Flash Size**: `4MB (FS:1MB OTA:~1019KB)`
  - **Erase Flash**: `All Flash Contents`

### Step 5: Upload the Firmware
- Connect your WeMos D1 Mini to your computer.
- Compile and upload the provided firmware using the **Upload** button in Arduino IDE.

---

<a name="usage"></a>

## 5. Usage

After successfully uploading the firmware, the device is ready to use. You can use the tactile push buttons to:

- **Scan Networks**: Discover nearby Wi-Fi networks.
- **Deauthenticate Devices**: Disconnect devices from a specific network.
- **Clone Networks**: Create fake access points to confuse users.

For a more detailed guide, you can refer to the **Zap Net Setup Tutorial** on [YouTube](https://youtu.be/BOveNABH84Y?si=lKpavXwBR5M6pI0-).

---

<a name="disclaimer"></a>

## 6. Disclaimer

**Warning**: The Zap Net Wi-Fi Deauther is a powerful tool designed for educational and ethical hacking purposes only. Using this device on any network without explicit permission from the network owner is illegal and can lead to serious legal consequences.

The examples and demonstrations have been created in a controlled, monitored environment with proper permissions.
---

## Credits

This project is heavily inspired by the original work done by [**Spacehuhn**](https://github.com/spacehuhn) on the **Deauther project**. 

We acknowledge the use of Spacehuhn’s open-source project under the **MIT License**.

---

### License

This project is licensed under the **MIT License**. See the `LICENSE` file for more details.

MIT License:


Copyright (c) 2024 C1PH3R-FSocitey

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
