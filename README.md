# IoT-based smart irrigation system using Raspberry Pi and NodeMCU with HTTP communication and ThingSpeak cloud integration.
# 🌱 Wireless Precision Irrigation System Using Raspberry Pi and NodeMCU

An IoT-based smart irrigation system that automates watering in multiple regions using Raspberry Pi (as the central gateway) and NodeMCUs (as sensor nodes). The system monitors soil moisture, temperature, humidity, and rainfall, and controls water flow based on real-time data. All readings are visualized on the ThingSpeak Cloud for remote monitoring.

# 📋 Project Overview

Traditional farming faces issues like inefficient water use, labor shortage, and climate challenges.
This project provides an automated irrigation solution that:

Collects environmental data through sensors

Transmits readings wirelessly using HTTP protocol

Uses Raspberry Pi as the main controller (server)

Controls water flow automatically via relay & solenoid valve

Uploads all data to ThingSpeak for visualization and analytics

# 🧠 System Architecture
Components Used:

Raspberry Pi (acts as gateway/server)

NodeMCU (ESP8266) – sensor node (acts as client)

DHT11 Sensor – temperature and humidity

Soil Moisture Sensor – detects soil dryness

Rain Sensor – detects rainfall

12V Solenoid Valve – controls water flow

Relay Module – for switching valve

12V Battery, connecting wires, and cables

RealVNC Viewer – for remote access to Raspberry Pi

# 🔗 Working Principle

Each NodeMCU reads sensor values (soil moisture, temperature, humidity, rain).

The data is sent to Raspberry Pi via HTTP POST request.

Raspberry Pi:

Receives and analyzes data from all regions

Decides irrigation status (ON/OFF) based on predefined logic

Sends control signals to relay for solenoid valve operation

Skips watering if rainfall is detected

All sensor data is sent to ThingSpeak Cloud for live monitoring and graph visualization.

The system can be remotely accessed using VNC Viewer.

# ⚙️ Software & Tools

Arduino IDE – for NodeMCU programming

Python (on Raspberry Pi) – to handle HTTP requests and relay control

ThingSpeak – IoT cloud for data visualization

RealVNC Viewer – for remote device access

# flow chart
![image alt](
