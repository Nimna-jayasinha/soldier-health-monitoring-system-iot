# Wiring Guide – Military Soldier Health Monitoring System (KENG-CV #007)

This guide outlines how to physically connect all sensors and modules to the ESP32 microcontroller. Refer to this along with the circuit diagram (`Schematics/circuit_diagram.png`) when assembling the hardware.

---

## 🧹 ESP32 Pin Configuration

| Sensor / Module          | ESP32 Pin | Type           | Description                          |
|--------------------------|-----------|----------------|--------------------------------------|
| Pulse Sensor             | GPIO32    | Analog Input   | Measures heart rate (BPM)            |
| LM35 Temperature Sensor  | GPIO34    | Analog Input   | Measures body temperature            |
| IR Sensor (Glove Check)  | GPIO35    | Analog Input   | Detects glove presence               |
| GPS RX (GPS TX → ESP32) | GPIO16    | UART RX        | Receives GPS signal from module      |
| GPS TX (ESP32 TX → GPS) | GPIO17    | UART TX        | Sends data to GPS module (if needed) |
| OLED SDA                 | GPIO21    | I2C Data       | Data line for OLED display           |
| OLED SCL                 | GPIO22    | I2C Clock      | Clock line for OLED display          |
| Common VCC               | 3.3V      | Power          | Power supply for all modules         |
| Common GND               | GND       | Ground         | Shared ground line for all modules   |

---

## ⚠️ Power Tips

- Use a **7V LiPo battery** or a USB cable connected to your computer or a power bank.
- Ensure all sensors are rated for **3.3V** operation if powered from ESP32.
- Avoid using 5V sensors unless verified compatible with ESP32 logic levels.

---

## 🔇 Connection Best Practices

- Use **dupont jumper wires** or soldered connections for stable builds.
- Ensure **tight and clean connections** to avoid noise and sensor misreadings.
- Place the **pulse sensor** securely on the finger for accurate data.
- Keep analog signal wires **away from power wires** to reduce interference.

---

## 🛠️ Assembly Order (Suggested)

1. Connect the **Pulse Sensor** to GPIO32
2. Connect **LM35** to GPIO34
3. Connect **IR Sensor** to GPIO35
4. Connect **GPS module** to GPIO16 (RX) and GPIO17 (TX)
5. Wire **OLED Display** to GPIO21 (SDA) and GPIO22 (SCL)
6. Power all components from **3.3V** and **GND**
7. Upload the code and power up the device

---

## 🧪 Testing Checklist

| Component        | Test                     |
|------------------|--------------------------|
| Pulse Sensor     | Values between 60–100 BPM |
| LM35             | Temperature in °C        |
| IR Sensor        | Detects glove distance   |
| GPS              | Shows live Lat/Lng       |
| OLED             | Displays values clearly  |

---

## 🔗 Reference

- See [`Docs/Blynk_Configuration.md`](./Blynk_Configuration.md) for cloud setup
- See [`Arduino_Code/KENG-CV-007_Military_Health_Monitor.ino`](../Arduino_Code/KENG-CV-007_Military_Health_Monitor.ino) for pin mappings in code

---

