# 🩺 Design and Development of an ESP-Based Wireless Nurse Calling System for Patient Care

<p align="center">
  <img src="images/Picture1.PNG" alt="AgriBot CAD Model" width="600"/>
</p>


## 🏥 Overview

This project presents a **wireless ESP-based Nurse Calling System** designed to improve communication between patients and nursing staff in hospitals and adult-care centers.  
The system replaces traditional wired nurse call systems with a **low-cost, flexible, and scalable wireless solution** that can be rapidly deployed in real hospital environments.

It is built using **ESP32** and **ESP8266 ESP-01** modules with optimized wireless configurations to ensure **long-range communication**, **low power consumption**, and **reliable nurse-station connectivity**.

<p align="center">
  <img src="images/nursecall_overview.png" alt="Wireless Nurse Calling System Overview" width="600"/>
</p>

---

## 🩺 Application Domain

The system is intended for:

- **Hospital wards**, especially where bed arrangements change frequently.  
- **Adult-care centers** with limited staff and high mobility requirements.
- Settings requiring **quick, portable, and inexpensive deployment** of nurse alert systems.

Key value additions:

- Eliminates costly hard-wired infrastructure.  
- Provides **portable remotes** that can be reassigned to any bed within seconds.  
- Improves **patient safety**, reducing response time and ensuring timely assistance.

---

## 🧠 Key Features & System Behaviour

### 📡 Wireless Communication Architecture

- Three wireless configurations were evaluated to determine the **most reliable communication method** for large hospital wards.  
- The final system uses a **router-based Wi-Fi LAN setup**, offering:
  - Extended range across long corridors.  
  - Stable signal quality (validated through RSSI experiments).  
  - Reliable TCP-based communication between patient remotes and the nurse station.  

<p align="center">
  <img src="images/nursecall_wifi_tests.png" alt="WiFi RSSI Experiments" width="600"/>
</p>

---

## 🧪 System Analysis & Experiments

### 📶 RSSI-Based Range Evaluation

To ensure stable performance in hospital corridors:

- Tested **direct ESP-to-ESP communication**,  
- Tested **intermediate-node communication**, and  
- Tested **router-based TCP communication**.  

The router-based configuration achieved **consistent communication up to ~90 m**, even through indoor environments 

### 🔋 Power Optimization for Battery-Based Remotes

- ESP modules were tested for **power usage during Wi-Fi initialization and data transmission**.  
- Average consumption per cycle:
  - **ESP32:** ~383 mW  
  - **ESP-01:** ~267 mW  
- A **power-saving trigger mechanism** was designed so remotes only power on during a button press, maximizing battery life.

---

## 🛠 Prototype Design & Fabrication

### 🧩 Patient Remote Unit

- Compact handheld remote with a large **emergency push button**.  
- **LED indicators** confirm that the signal was successfully sent and acknowledged.  
- Designed for **simple one-button operation**, ideal for elderly or critically ill patients.  

### 🖥️ Nurse Station Unit

- Displays the **bed number** of the patient requesting help.  
- Provides **visual indicators** and **audible alerts** via LED and buzzer.  
- Built with a **sheet-metal enclosure** for durability and clinical usability.  

<p align="center">
  <img src="images/nursecall_station.png" alt="Nurse Station Device" width="450"/>
</p>

---

## 🧪 Real-World Validation

The system was tested in a **Sri Lankan hospital ward** 

- Reliable communication across the entire ward layout.  
- Flexibility to **reassign remotes to different beds** without any hardware modification.  
- Consistent performance under real patient-care conditions.

<p align="center">
  <img src="images/nursecall_station.png" alt="Nurse Station Device" width="450"/>
</p>

---

## 📦 Tools & Technologies

- `ESP32` and `ESP8266 ESP-01` for wireless communication  
- `Wi-Fi LAN (router-based)` for long-range reliability  
- `3D printing` for remote casing fabrication  
- `Sheet metal enclosure` for nurse station  
- `MATLAB` for RSSI curve fitting and analysis  

---
