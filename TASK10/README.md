# Smart Soil Moisture Monitoring and Automatic Irrigation System

## Overview

The Smart Soil Moisture Monitoring and Automatic Irrigation System is an IoT-based project developed using an ESP32, soil moisture sensor, relay module, and WiFi connectivity. The system continuously monitors soil moisture levels and automatically controls irrigation based on predefined threshold values. Real-time sensor data is transmitted to the Zelbytes IoT Dashboard for remote monitoring and visualization.

## Features

* Automatic irrigation based on soil moisture level
* Manual override using a push button
* Serial commands for monitoring and control
* WiFi connectivity using ESP32
* Cloud telemetry integration with Zelbytes IoT Dashboard
* LED indication for pump status
* Real-time data monitoring and visualization

## Components Used

* ESP32 Development Board
* Soil Moisture Sensor
* Relay Module
* Water Pump
* Push Button
* LED
* 220 Ω Resistor
* Jumper Wires
* External Power Supply

## Pin Connections

| Component               | ESP32 Pin |
| ----------------------- | --------- |
| Soil Moisture Sensor A0 | GPIO34    |
| Relay Module IN         | GPIO26    |
| Push Button             | GPIO27    |
| LED                     | GPIO2     |

## Working Principle

The soil moisture sensor continuously measures the moisture content of the soil and sends analog readings to the ESP32. In automatic mode, the ESP32 compares the sensor value with a predefined threshold and activates the relay when the soil becomes dry. Once sufficient moisture is detected, the relay turns off the pump. Manual control is provided through a push button and serial commands. Sensor data is uploaded to the Zelbytes IoT Dashboard over WiFi for real-time monitoring and historical analysis.

## Serial Commands

* `STATUS` – Displays current soil moisture, pump status, and operating mode.
* `FORCE_ON` – Forces the pump ON and enters manual mode.
* `FORCE_OFF` – Forces the pump OFF and enters manual mode.

## Applications

* Smart Agriculture
* Home Gardening
* Greenhouse Monitoring
* Automated Irrigation Systems

## Conclusion

This project demonstrates an efficient and reliable IoT-based irrigation system capable of automatic watering and cloud-based monitoring. It provides an effective solution for water management and smart agriculture applications.
