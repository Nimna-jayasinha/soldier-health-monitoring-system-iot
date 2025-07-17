# Blynk Cloud Setup – Military Soldier Health Monitoring System (KENG-CV #007)

This document guides you through setting up Blynk Cloud to work with the ESP32-based health monitoring system.

---

## 💠 Step-by-Step Blynk Setup

1. **Sign Up or Log In** to [Blynk.Cloud](https://blynk.cloud).

2. Create a **New Template**:

   - Template Name: *Military Soldier Health Monitoring System*
   - Device Type: *ESP32*

3. After creating the template, note the generated:

   - **Template ID**
   - **Template Name**
   - **Auth Token**

4. **Add a New Device** using this template.

5. Use the Auth Token, Template ID, and Template Name in your Arduino code:

```cpp
#define BLYNK_TEMPLATE_ID "YOUR_TEMPLATE_ID"
#define BLYNK_TEMPLATE_NAME "YOUR_TEMPLATE_NAME"
#define BLYNK_AUTH_TOKEN "YOUR_AUTH_TOKEN"
```

> Replace `"YOUR_..."` with your own credentials from Blynk.

---

## 📲 Blynk Virtual Pin Mapping

| Parameter        | Virtual Pin | Suggested Widget Type |
| ---------------- | ----------- | --------------------- |
| Heart Rate (BPM) | V0          | Gauge / Chart         |
| Temperature (°C) | V1          | Gauge                 |
| GPS Location     | V2          | Label                 |
| Glove Status     | V3          | Label / Notification  |

---

## ⚙️ Sensor to ESP32 Pin Configuration

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

## 💽 Dashboard Widgets Example

Add the following widgets to your Blynk template dashboard:

- **Gauge** for Heart Rate → V0
- **Gauge** for Temperature → V1
- **Label** for GPS Location → V2
- **Label** or **Notification** for Glove Status → V3

> Optional: Add a **Chart** to visualize heart rate or temperature trends.

---

## 💡 Tips

- Test each sensor individually before integration.
- Ensure the ESP32 board is selected properly in Arduino IDE.
- Use 3.3V for all sensors unless marked 5V-compatible.
- Place pulse sensor firmly on finger for accurate readings.

---

## 📌 Related Files

- Wiring: [`Docs/Wiring_Guide.md`](./Wiring_Guide.md)
- Arduino Code: [`Arduino_Code/KENG-CV-007_Military_Health_Monitor.ino`](../Arduino_Code/KENG-CV-007_Military_Health_Monitor.ino)

---

This guide ensures easy reconfiguration of the system without sharing any private keys or network information.

