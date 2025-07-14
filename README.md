

# 🌱 Smart Agriculture Assistant – M5Stack Code

This repository contains the embedded code for the **Smart Agriculture Assistant**, developed using **MicroPython** and **UIFlow** for the **M5Stack Core** IoT device. The system is designed to support small-scale farming by providing real-time environmental monitoring, irrigation alerts, and intrusion detection.

## 🚀 Features

* 🌡️ **Environmental Monitoring**:
  Uses the **ENV III Unit** to measure:

  * Temperature
  * Humidity
  * Barometric Pressure

* 🚨 **Intrusion Detection**:

  * Detects motion using the **PIR sensor**
  * Triggers **buzzer** and **RGB LED** for real-time alerts

* 💧 **Irrigation Assistant**:

  * Sends alerts if temperature/humidity thresholds suggest watering is needed
  * Can be enhanced with weather APIs (for weather-aware decisions)

* 📡 **Real-time Data Transmission**:

  * Sends sensor data via HTTP (POST/GET) to a Flask-based backend server
  * Designed for easy integration with a web dashboard (Chart.js visualizations)

---

## 🔧 Hardware Used

| Module          | Description                                   |
| --------------- | --------------------------------------------- |
| M5Stack Core    | Main IoT controller (ESP32-based)             |
| ENV III Unit    | Environmental sensor (Temp/Humidity/Pressure) |
| PIR Sensor Unit | Motion detection sensor                       |
| RGB LED Unit    | Visual alerts                                 |
| Buzzer Unit     | Audible alerts                                |



---

## 📡 Connectivity

* Wi-Fi credentials are stored in `wifi_config.py`
* Data is posted every X seconds to the backend API endpoint `/api/data`
* Update `http_client.py` to match your Flask server IP or domain

---

## 🧠 Future Enhancements

* Integrate with weather APIs for smarter irrigation suggestions
* Add ML-based anomaly detection using historical sensor data
* OTA updates and MQTT support for cloud deployment

---


