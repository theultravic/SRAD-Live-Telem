# SRAD-Live-Telem
SRAD Flight Computer for live telemetry.

## Overview

This project is a custom-built **Live Telemetry System** designed for high-power rocketry applications. Built around the **Teensy 4.1** microcontroller, it captures and transmits real-time data during flight using onboard sensors, SD logging, and a dedicated radio telemetry link. A secondary system handles **live video streaming** from the vehicle to ground stations.

The system is built to withstand high-G acceleration environments (up to 30+ Gs), and the design emphasizes robustness, modularity, and future compatibility with avionics used in competitions like **IREC**.

---

## 📦 Features

- 🔧 **Microcontroller:** Teensy 4.1 (600 MHz ARM Cortex-M7)
- 🔋 **Voltage Regulators:** Pololu 5V Step-Up Regulator U3V50F5 (5V @ up to 1.5A) & Pololu 3.3V Step-Down Regulator D24V5F3 (3.3V @ 500 mA)
- 📈 **Sensor Suite:**
  - **IMU:** 9-DOF Gyroscope + Accelerometer (LSM6DSOX)
  - **Barometer:** High-altitude capable (MS5611-01BA03)
  - **RTC:** DS3231 for onboard timestamping
  - **Pressure Transducer: **P51-1000-A-B-I36-5V**
- 💾 **Storage:** Teensy built in microSD might integrate redundant SD card
- 📡 **Telemetry:** 433 MHz or 915 MHz transmitter (RFM95 LoRa)
- 📹 **Live Video:** Raspberry Pi Zero/Camera + analog/digital video TX (*Maybe*)
- 🔋 **Power:** LiFePO4 pack with voltage regulation for subsystems
- 🛠 **Vibration & Shock Damping:** Silicone mounts for PCB and SD module protection

---

## 📊 Live Data Tracked

- Altitude (barometric and integrated)
- Vertical velocity and acceleration
- 3-axis gyro and accel data (for post-flight analysis)
- Orientation estimation (future: Kalman or complementary filter)
- System timestamp
- GPS (*Maybe*)
- Motor pressure
- Battery voltage and system status
