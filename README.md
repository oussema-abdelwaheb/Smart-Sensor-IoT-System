# Smart Sensor IoT System (ESP32 + MQTT + Raspberry Pi 5)

This project was developed during my internship at **YUCCAINFO** (July–August 2025).  
It implements a **distributed IoT sensing system** where multiple ESP32-based smart sensors send data to a central **MQTT broker** on a **Raspberry Pi 5**, with logging and dashboard visualization.

---

## 📡 System Overview
- **ESP32 Smart Sensors**: Acquire, process, and condition environmental data.  
- **Communication Approaches**:  
  - Initial prototype with **BLE** → unstable connections, authentication issues.  
  - Final solution with **ESP-NOW** → stable, low-power, scalable.  
- **Central ESP32 Node**: Receives ESP-NOW packets and relays them via Wi-Fi to MQTT.  
- **Raspberry Pi 5**: Runs the MQTT broker, logs messages to text files, and provides a real-time dashboard.  

---

## 🛠️ Features
- Deep sleep on ESP32 nodes for **low power consumption**.  
- Secure communication with **handshake + MAC filtering**.  
- **Reliable multi-node support** using ESP-NOW.  
- **Real-time monitoring dashboard** with Node-RED / Grafana.  
- Persistent **data logging** to text files.  

---

## 🚀 Getting Started
1. Flash ESP32 firmware from `firmware/sensor_node` and `firmware/central_node`.  
2. Set up MQTT broker on Raspberry Pi (`raspberry_pi/mqtt_broker_setup.md`).  
3. Run logger script and open dashboard for real-time monitoring.  
4. Deploy multiple nodes → observe data streams in real time.  

---

## 📂 Repository Contents
- `firmware/` → ESP32 code (BLE prototype + ESP-NOW final version).  
- `raspberry_pi/` → Broker setup, logger script, dashboard configs.  
- `docs/` → Architecture diagram and documentation notes.  

---

## 🙏 Acknowledgements
Special thanks to my supervisor, **Mr. Mahdi Abdessalam**, for his mentorship and guidance during this project.  

---

## 📌 Future Work
- Add **edge AI** to ESP32 nodes.  
- Extend to **industrial IoT applications**.  
- Improve encryption and secure storage.  

