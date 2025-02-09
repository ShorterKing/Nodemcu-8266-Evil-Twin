# WiFi Evil Twin Attack - Fully Functional Captive Portal

![WiFi Evil Twin](https://img.shields.io/badge/ESP8266-NODEMCU-blue) ![Captive Portal](https://img.shields.io/badge/Captive%20Portal-Working-green) ![WiFi Attack](https://img.shields.io/badge/WiFi%20Evil%20Twin-Advanced-red)

## ⚡ About This Project
This is a **fully functional** WiFi Evil Twin attack using **NodeMCU ESP8266** that works on **both PC and mobile devices**. Unlike many other projects, the **captive portal actually works** with proper password verification, making it one of the most reliable Evil Twin projects available. 

> **DISCLAIMER:** This project is for **educational and security research purposes only**. Unauthorized use of this software to intercept or manipulate WiFi networks without explicit permission is illegal and punishable by law. Use responsibly!

---

## 🚀 Features
✅ **Works on both PC and mobile devices**
✅ **Fully functional Captive Portal** with password verification
✅ **Automatic deauthentication attack** to disconnect users from the real network
✅ **Customizable SSID & Captive Portal** page
✅ **Logs captured passwords** for analysis
✅ **Lightweight and runs on NodeMCU ESP8266**
✅ **Restarts the original access point upon correct password entry**
✅ **View captured credentials by reconnecting to the original network or visiting `/admin`**

---

## 📜 Requirements
- **NodeMCU ESP8266**
- **Arduino IDE** (for flashing the `.ino` file)
- **ESP8266WiFi Library** (installed in Arduino IDE)

---

## 🔧 Installation & Setup
### 📌 Method 1: Flash Using Arduino IDE
1. Download and install **Arduino IDE** from [here](https://www.arduino.cc/en/software).
2. Install the **ESP8266 Board Manager**:
   - Open Arduino IDE and go to `File` > `Preferences`
   - Add the following URL to **Additional Board Manager URLs**:
     ```
     http://arduino.esp8266.com/stable/package_esp8266com_index.json
     ```
   - Go to `Tools` > `Board` > `Boards Manager`, search for **ESP8266**, and install it.
3. Install required libraries:
   - Open `Sketch` > `Include Library` > `Manage Libraries`
   - Search for and install `ESP8266WiFi`
4. Open the `.ino` file from this repository in Arduino IDE.
5. Select **Board: NodeMCU 1.0 (ESP-12E Module)** and correct **COM Port**.
6. Click **Upload** and wait for the process to complete.

### 📌 Method 2: Flash Prebuilt Release (Recommended)
1. Download the latest **.bin** release from the [Releases](https://github.com/YOUR_GITHUB_USERNAME/WiFi-Evil-Twin/releases) page.
2. Use **esptool.py** or any ESP8266 flasher to flash the firmware:
   ```bash
   esptool.py --port /dev/ttyUSB0 write_flash -fm dio 0x00000 firmware.bin
   ```
   *(Replace `/dev/ttyUSB0` with the correct port)*

---

## 🛠 Usage
1. **Power on** the ESP8266 module.
2. The fake WiFi network (Evil Twin) will appear.
3. When a victim connects, they will be redirected to the **captive portal**.
4. Once they enter their **WiFi password**, it is logged and stored.
5. If the password is correct, the **NodeMCU restarts the original access point**.
6. You can check the captured credentials by **connecting to the original network** or visiting `/admin` on the access point.

---

## ⚠️ Legal Disclaimer
This project is intended **ONLY** for educational purposes and authorized penetration testing. **Do not use this tool on unauthorized networks.** The developer is **not responsible** for any misuse.

---

## 📜 License
This project is licensed under the **MIT License**. Feel free to modify and distribute, but always give credit!

---

## 🤝 Contributing
Pull requests are welcome! If you find bugs or want to add improvements, feel free to submit a PR.

---

## 📬 Contact
For any queries or discussions, feel free to open an issue or reach out on **GitHub**.

🎯 **Enjoy Ethical Hacking & Stay Secure!**

