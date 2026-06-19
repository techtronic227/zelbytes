# Smart Soil Moisture Monitoring and Automatic Irrigation System

## Overview

This project implements an IoT-based smart irrigation system using an ESP32, soil moisture sensor, relay module, and water pump. The system continuously monitors soil moisture and automatically controls irrigation based on a predefined threshold. Manual control is provided through a push button and serial commands. Sensor readings are uploaded to the Zelbytes IoT Dashboard over Wi-Fi for real-time monitoring and visualization.

## Features

* Automatic irrigation based on soil moisture level
* Manual override using a push button
* Serial commands for monitoring and control
* Wi-Fi connectivity using ESP32
* Real-time telemetry upload to Zelbytes IoT Dashboard
* LED indication for pump status
* Built-in web server for remote control

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

| Component       | ESP32 Pin |
| --------------- | --------- |
| Soil Sensor A0  | GPIO34    |
| Relay IN        | GPIO26    |
| Push Button     | GPIO27    |
| LED             | GPIO2     |
| Soil Sensor VCC | 3.3V      |
| Relay VCC       | 5V        |
| Common Ground   | GND       |

## Working Principle

The soil moisture sensor measures the moisture content of the soil and sends analog values to the ESP32. In automatic mode, the ESP32 compares the sensor value with a threshold and activates the relay when the soil becomes dry. The relay switches the water pump on and off accordingly. Users can manually control the pump using a push button or through serial commands. Sensor data is transmitted over Wi-Fi to the Zelbytes IoT Dashboard for visualization and analysis.

## Serial Commands

* `STATUS` – Displays current soil moisture, pump status, and mode.
* `FORCE_ON` – Forces the pump ON and enters manual mode.
* `FORCE_OFF` – Forces the pump OFF and enters manual mode.

## Applications

* Smart agriculture
* Home gardening
* Greenhouse monitoring
* Water-efficient irrigation systems
