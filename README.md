# 🛡️ Military Soldier Health Monitoring System (KENG-CV #007)

A real-time IoT-based health and safety monitoring system for military soldiers using ESP32 and Blynk Cloud. This system continuously monitors heart rate, temperature, GPS location, and glove status, and displays the data on a web dashboard via Blynk Cloud.

---

## 📌 Project Overview

This system helps track vital signs of soldiers on the field, ensuring real-time health and safety updates to the command center.

**Main Features:**

- Real-time heart rate monitoring with Pulse Sensor
- Body temperature measurement using LM35
- GPS-based location tracking
- Glove detection via IR sensor for safety compliance
- OLED display for local viewing
- Blynk dashboard for cloud-based monitoring

---

## 🚀 Getting Started

### Hardware Requirements:

- ESP32 Dev Board
- Pulse Sensor
- LM35 Temperature Sensor
- NEO-6M GPS Module
- IR Sensor
- 0.96" I2C OLED Display (128x64)

### Software Requirements:

- Arduino IDE
- Required Libraries:
  - `WiFi.h`, `Wire.h`, `BlynkSimpleEsp32.h`
  - `Adafruit_SSD1306`, `Adafruit_GFX`
  - `PulseSensorPlayground`, `TinyGPS++`

---

## 🔌 Pin Configuration

| Sensor / Module          | ESP32 Pin | Description                      |
| ------------------------ | --------- | -------------------------------- |
| Pulse Sensor             | GPIO32    | Analog input for BPM             |
| LM35 Temperature Sensor  | GPIO34    | Analog input for temperature     |
| IR Sensor (Glove Detect) | GPIO35    | Analog input for glove detection |
| GPS RX                   | GPIO16    | Receives GPS data                |
| GPS TX                   | GPIO17    | Sends GPS data                   |
| OLED SDA                 | GPIO21    | I2C data line                    |
| OLED SCL                 | GPIO22    | I2C clock line                   |

---

## 🌐 Blynk Dashboard Setup

Refer to [`Docs/Blynk_Configuration.md`](./Docs/Blynk_Configuration.md) for full details on:

- Creating the Blynk template
- Mapping virtual pins
- Adding widgets to the dashboard

---

## 📁 Folder Structure

```
📆Military Soldier Health Monitoring System
🔜 Arduino_Code
🔜 Docs
🔜 Reports
🔜 Images
├── .gitignore
├── LICENSE
└── README.md
```

---

## 📸 Output Dashboard



---

## 🎓 Course Info

This project was developed as part of:

- **Course:** IoT-Based Embedded Systems Design
- **Institution:** [Your University Name]
- **Group Code:** KENG-CV #007
- **Team Members:**
  - Madushan Sandaruwan – Embedded Developer
  - [Add other members if any]

---

## 🤝 Contributions

Contributions are welcome! Please fork the repo and submit a pull request for improvements.

---

## 📜 License

This project is licensed under the [MIT License](./LICENSE).

---

## 📞 Contact

For questions or support, please contact:

- Madushan Sandaruwan – [[your\_email@example.com](mailto\:your_email@example.com)]

