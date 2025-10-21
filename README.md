# IoT-based smart irrigation system using Raspberry Pi and NodeMCU with HTTP communication and ThingSpeak cloud integration.
# 🌱 Wireless Precision Irrigation System Using Raspberry Pi and NodeMCU

An IoT-based smart irrigation system that automates watering in multiple regions using Raspberry Pi (as the central gateway) and NodeMCUs (as sensor nodes). The system monitors soil moisture, temperature, humidity, and rainfall, and controls water flow based on real-time data. All readings are visualized on the ThingSpeak Cloud for remote monitoring.

# 📋 Project Overview

Traditional farming faces issues like inefficient water use, labor shortage, and climate challenges.
This project provides an automated irrigation solution that:

- Collects environmental data through sensors

- Transmits readings wirelessly using HTTP protocol

- Uses Raspberry Pi as the main controller (server)

- Controls water flow automatically via relay & solenoid valve

- Uploads all data to ThingSpeak for visualization and analytics

# 🧠 System Architecture
### Components Used:

1.Raspberry Pi (acts as gateway/server)

2.NodeMCU (ESP8266) – sensor node (acts as client)

3.DHT11 Sensor – temperature and humidity

4.Soil Moisture Sensor – detects soil dryness

5.Rain Sensor – detects rainfall

6.12V Solenoid Valve – controls water flow

7.Relay Module – for switching valve

8.12V Battery, connecting wires, and cables

9.RealVNC Viewer – for remote access to Raspberry Pi

# 🔗 Working Principle

1.Each NodeMCU reads sensor values (soil moisture, temperature, humidity, rain).

2.The data is sent to Raspberry Pi via HTTP POST request.

### Raspberry Pi:

3.Receives and analyzes data from all regions

4.Decides irrigation status (ON/OFF) based on predefined logic

5.Sends control signals to relay for solenoid valve operation

6.Skips watering if rainfall is detected

7.All sensor data is sent to ThingSpeak Cloud for live monitoring and graph visualization.

8.The system can be remotely accessed using VNC Viewer.

# ⚙️ Software & Tools

- Arduino IDE – for NodeMCU programming

- Python (on Raspberry Pi) – to handle HTTP requests and relay control

- ThingSpeak – IoT cloud for data visualization

- RealVNC Viewer – for remote device access

# flow chart
![image alt](https://github.com/SatishBabuKukkapalli/wireless-precision-irrigation-system/blob/086e42737907e387193919f5cc1a63347c44a978/fc.jpg)

# How HTTP Works in Our Smart Irrigation Project?
- Each NodeMCU acts as a client:
  - It reads data from sensors (soil moisture, rain, DHT11).
  - It sends this data using HTTP POST requests to the Raspberry Pi.
- The Raspberry Pi acts as a server:
  - It receives the HTTP data from each NodeMCU.
  - It analyzes the data to decide whether watering is needed.
- Based on the data, Raspberry Pi:
  - Sends a signal to the relay to turn the solenoid valve ON/OFF.
  - Time duration for watering is based on how many regions report dryness.
  - If it's raining, watering is skipped.

# Block diagram
![image alt](https://github.com/SatishBabuKukkapalli/wireless-precision-irrigation-system/blob/c15397e994567fa85ce03bf4769a1e80be0399e7/proposed%20system.jpg)

## 💻 Code Overview

### NodeMCU Code (Client)
- Reads sensor values
- Sends data to Raspberry Pi using HTTP POST

### Raspberry Pi Code (Server)
- Receives HTTP data from NodeMCUs
- Applies delay logic for irrigation
- Sends data to ThingSpeak
- Controls relay for solenoid valve

# outputs
### Harware setup
![image alt](https://github.com/SatishBabuKukkapalli/wireless-precision-irrigation-system/blob/df12e9836b373d9c419a6a19dc1c395e34fb5de2/hardware%20setup.jpg)
### Result
![image alt]
