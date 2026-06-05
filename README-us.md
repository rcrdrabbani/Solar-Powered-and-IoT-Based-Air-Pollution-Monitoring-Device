# Solar-Powered & IoT-Based Air Pollution Monitoring Device 🌍☀️

[![IoT](https://img.shields.io/badge/IoT-Platform-blue.svg)]()
[![Hardware](https://img.shields.io/badge/Hardware-ESP32%20%7C%20ESP8266-orange.svg)]()
[![Language](https://img.shields.io/badge/Language-C++%20%7C%20Python-green.svg)]()

An advanced, self-sustaining IoT edge-device designed to monitor real-time air quality metrics. This system operates autonomously using solar energy and orchestrates complex state-handling for continuous environmental data streaming.

---

## 🇺🇸 English Version

### 📌 Project Overview
This project bridges the gap between hardware power-efficiency and modern cloud analytics. Built as an engineering capstone, the device utilizes a photovoltaic (PV) system to maintain 24/7 uptime in remote areas, compiling particulate and gas telemetry into compact data packets transmitted directly to cloud infrastructure.

### 🏗️ System Architecture
The firmware is structured using a **Finite State Machine (FSM)** layout to eliminate looping blocking states and handle sensor warm-ups, network drops, and power-saving modes gracefully.

* **Edge Device:** ESP32 / ESP8266 microcontroller fetching raw analog/digital data from electrochemical sensors.
* **Data Pipeline:** Raw metrics are structured into lightweight `JSON` payloads.
* **Cloud Gateway:** A Python script manages the REST API handshakes, ingesting telemetry streams into a live database.
* **Dashboard:** Integrated via Google Sheets API for real-time visualization and historic logging.

### 🛠️ Technical Stack
* **Hardware & Power:** ESP32, Solar Panel, Solar Charge Controller (SCC), Li-ion Battery Storage, Electrochemical Sensors.
* **Firmware:** C/C++ (Arduino IDE), FSM Architecture, Optimized Power Management.
* **Software & Integration:** Python Scripting, JSON Parser, REST API, Google Sheets API.
* **Mechanical & Design:** EasyEDA (PCB Design), Autodesk CAD (Enclosure Scheme).

---
