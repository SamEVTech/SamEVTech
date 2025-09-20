# 🔆 Dual-Axis Solar Tracker

Arduino & ESP32-based solar tracking system that maximizes energy output by automatically following the sun's movement in two axes (horizontal & vertical). Designed for EV charging stations and off-grid solar applications.

[![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white)](https://arduino.cc)
[![ESP32](https://img.shields.io/badge/ESP32-3C92D3?style=for-the-badge&logo=esp32&logoColor=white)](https://espressif.com)
[![Solar](https://img.shields.io/badge/Solar-Energy-FFD700?style=for-the-badge&logo=sun&logoColor=black)](https://en.wikipedia.org/wiki/Solar_energy)

---

## 📖 Project Overview

### 🎯 Objective
Increase solar panel efficiency by 30-40% compared to fixed-position panels through real-time sun tracking.

### 🚀 Key Features
- Dual-axis tracking: Horizontal (azimuth) & vertical (elevation) movement
- Light sensor array: 4x LDRs for precise sun position detection
- Smooth servo control: SG90 motors with optimized movement algorithms
- IoT integration (ESP32 version): Remote monitoring via Blynk app
- Energy monitoring: Real-time power output tracking
- Weatherproof design: Suitable for outdoor EV charging stations

### 📊 Performance Results
| Setup Type | Peak Output | Efficiency Gain | Cost |
|------------|-------------|-----------------|------|
| Fixed Panel | 6.2W | Baseline (100%) | ₹500 |
| Single-Axis Tracker | 7.1W | +15% | ₹1200 |
| Dual-Axis Tracker | 8.4W | +35% | ₹1800 |

---

## 🛠️ Technical Specifications

### 📸 Hardware Components
| Component | Quantity | Specifications | Approx. Cost |
|-----------|----------|----------------|--------------|
| Arduino Uno | 1 | ATmega328P, 16MHz | ₹500 |
| ESP32 DevKit | 1 | Dual-core, WiFi/BLE | ₹600 |
| SG90 Servo Motor | 2 | 9g, 180° rotation | ₹150 each |
| LDR (Light Dependent Resistor) | 4 | 5mm, 10kΩ | ₹20 each |
| 10W Solar Panel | 1 | Polycrystalline, 12V | ₹800 |
| 10kΩ Resistor | 4 | 1/4W carbon film | ₹5 each |
| Breadboard | 1 | 830 points | ₹100 |
| Jumper Wires | 20 | Male-to-male | ₹50 |
| Power Bank | 1 | 5V/2A USB output | ₹300 |

Total Estimated Cost: *₹2500* (₹1800 without solar panel)

### ⚙️ Software Stack
- Arduino IDE v1.8.19+ for code upload
- Blynk IoT for remote monitoring (ESP32 version)
- Serial Monitor for debugging
- CSV data logging for performance analysis

---

## 🔌 Circuit Diagram & Wiring

### 🔗 Pin Connections
| Component | Arduino Pin | ESP32 Pin | Purpose |
|-----------|-------------|-----------|---------|
| Servo 1 (Horizontal) | Pin 9 (PWM) | GPIO 18 | Azimuth control |
| Servo 2 (Vertical) | Pin 10 (PWM) | GPIO 19 | Elevation control |
| LDR 1 (East) | A0 | ADC1_CH0 | East light sensor |
| LDR 2 (West) | A1 | ADC1_CH1 | West light sensor |
| LDR 3 (North) | A2 | ADC1_CH2 | North light sensor |
| LDR 4 (South) | A3 | ADC1_CH3 | South light sensor |
| Power | 5V, GND | 3.3V, GND | Power supply |

---

## 💻 Complete Arduino Code

### 🌟 Main Code: solar_tracker.ino

File: solar_tracker.ino (neeche alag section mein code hai)

---

## 🔧 Setup & Installation Guide

### 📋 Step-by-Step Assembly

1. Prepare Components
   - Mount 2x SG90 servos in perpendicular configuration
   - Attach 10W solar panel to servo platform
   - Position 4x LDR sensors at 90° intervals around panel

2. Code Upload
   - Open Arduino IDE → File → Open → solar_tracker.ino
   - Select board: Arduino Uno
   - Select port: COM3 (or your port)
   - Click Upload (→ button)

3. Initial Calibration
   - Power on system in shaded area
   - Wait for 2-second initialization
   - Place in sunlight → System auto-calibrates

---

## 📈 Testing & Results

### 📊 Performance Data

| Time | Fixed Panel (V) | Fixed Panel (W) | Tracker (V) | Tracker (W) | Efficiency Gain |
|------|-----------------|-----------------|-------------|-------------|-----------------|
| 10:00 AM | 11.8V | 4.2W | 11.9V | 4.8W | +14% |
| 12:00 PM | 12.3V | 6.2W | 12.4V | 8.4W | +35% |
| 2:00 PM | 11.5V | 4.8W | 11.7V | 6.1W | +27% |
| 4:00 PM | 10.2V | 2.9W | 10.5V | 3.8W | +31% |

Average Daily Gain: *+26.75% | *Total Extra Energy: **1.8 kWh/year

---

## 🚀 Applications & Use Cases

### 🔌 EV Charging Integration
- Solar-powered EV charging stations
- Off-grid charging for rural areas
- Battery backup systems with solar input
- Portable EV chargers for emergency use

---

## 🛠️ Troubleshooting Guide

| Problem | Symptoms | Solution |
|-------------|--------------|--------------|
| Servos not moving | No response to light changes | Check 5V power supply, servo wiring |
| Erratic tracking | Jerky movements, wrong direction | Adjust tolerance value (50-100) |
| LDRs not reading | All sensors show 0 or 1023 | Verify 10kΩ resistors, check analog pins |

---

## 📄 License & Credits

### 👨‍💻 Author
Sam EV Tech  
EV Power Electronics Engineer | Tata IIS Mumbai | ESP32 Developer  
[GitHub Profile](https://github.com/SamEVTech) | [LinkedIn](https://linkedin.com/in/Sam-EVTech)

<div align="center">
  <img src="https://img.shields.io/badge/Status-Working%20Prototype-brightgreen?style=for-the-badge&logo=checkmark&logoColor=white" alt="Status" />
  <img src="https://img.shields.io/badge/Efficiency-Gain%2035%25-orange?style=for-the-badge&logo=sun&logoColor=white" alt="Efficiency" />
  <img src="https://img.shields.io/badge/Cost-%25E2%82%B91800-blue?style=for-the-badge&logo=money&logoColor=white" alt="Cost" />
</div>

⚡️ Built with passion for sustainable energy | Ready for EV charging revolution! 🚀
