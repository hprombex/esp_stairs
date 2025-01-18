
# 🌈 ESP_Stairs - Stairs Lighting Automation Project 🌈

## 📋 Project Overview
This repository contains the code and resources for automating stairs lighting using ESP32 and WS2812b LEDs.

**Project Status:** Work in Progress 🚧 

---

## ✨ Features
- **Individually Addressable LEDs**: Each step has a predefined range of LEDs for precise control.
- **Custom Lighting Effects**: Preconfigured effects to enhance the lighting experience.
- **Motion Detection**: PIR sensors trigger lights for specific steps.
- **Persistent State**: Last light state and RGB color values are restored after power loss.
- **Web Interface**: Accessible web server for control and configuration.
- **Secure Communication**: Supports OTA updates, API encryption, and manual IP configuration.

---

## 🔧 Configuration Overview
### Substitutions
- **Transition Times**: Adjustable transitions for smooth lighting changes.
- **Delays**: Fine-tuned delays for motion-triggered light activations.
- **LED Properties**: Define the LED type, gamma correction, and total count.
- **Step Ranges**: Predefined LED ranges for each staircase step.

### ESP32 Board Setup
The project uses an ESP32 development board with:
- GPIO pins for LED data and PIR sensors.

---

## 🛠️ Hardware Requirements
1. **ESP32 Development Board**
2. **WS2812B LED Strip**
3. **PIR Motion Sensors (e.g., AM312)**: Positioned at strategic points along the staircase.
4. **Power Supply**: Capable of handling the LED strip's power requirements.
5. **Other**: TI 74AHCT125, UART TTL on RS485 (MAX485)

---

## 🧰 Installation
### 1. Prerequisites
- Clone this repository:
   ```bash
   git clone https://github.com/hprombex/esp_stairs.git
   ```
- Install via ESPHome.

### 2. Flash the ESP32
- Use the ESPHome CLI:
  - Plug in the device via USB and type the command:
  ```bash
  esphome run esp-stairs.yaml
   ```
  After the first upload, you will probably never need to use the USB cable again

  [Getting Started with the ESPHome Command Line](https://esphome.io/guides/getting_started_command_line.html)

  [Command Line Interface](https://esphome.io/guides/cli.html)


- Dashboard to flash the ESP32 with this configuration.

### 3. Wiring
- Connect the LED strip's data pin to `GPIOXX` on the ESP32.
- Attach PIR sensors to their respective GPIO pins.
- Power the ESP32 and LED strip with an adequate power supply.

### 4. Configure Secrets
Create/Configure a `secrets.yaml` file in the same directory and include:
```yaml
wifi_ssid: "<Your Wi-Fi SSID>"
wifi_password: "<Your Wi-Fi Password>"
web_server_username: "<Web Server Username>"
web_server_password: "<Web Server Password>"
esp_stairs_api_key: "<API Encryption Key>"
esp_stairs_ota_password: "<OTA Password>"
esp_stairs_ip: "<Static IP Address>"
```

---

## 🖥️ Usage
🚧 *Placeholder* 🚧

---

## 🎥 YouTube
🚧 *Placeholder for video tutorials and demonstrations.* 🚧

---

## 🧩 Connection Schematics
🚧 *Placeholder for connection diagrams and wiring instructions.* 🚧

---

## 🤖 3D models
🚧 *Placeholder for 3D models.* 🚧

---

## ⚠️ Troubleshooting
**Common Issues:**
- **Issue:** False positives from PIR sensors.  
  🛠️ **Solution:** Verify the placement of sensors and shield them from LED interference.

- **Issue:** LEDs flicker or do not light up.  
  🛠️ **Solution:** Check the power supply and connections. Ensure the data signal is stable.

- **Issue:** Memory Issues.  
  🛠️ **Solution:**  Adjust the logger level or disable it to save memory: ```level: NONE```

---

## 🎯 Future Enhancements
- Add more complex lighting effects.
- ...

---

## 📜 License
This project is licensed under the MIT License. See the LICENSE file for details.

---
For further assistance or contributions, feel free to open an issue or submit a pull request.
```
