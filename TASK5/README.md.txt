# Task 5: Threshold Logic and State Machine for Smart Irrigation

## Overview

This project implements an automatic irrigation system using a finite state machine. The system monitors soil moisture and environmental conditions to control irrigation efficiently. When the soil becomes dry, the relay activates the solenoid valve and irrigation begins. An LED indicator is used to show the irrigation status.

## Working Principle

The Arduino continuously reads the soil moisture level and the temperature and humidity values from the DHT22 sensor. If the soil moisture falls below the specified threshold, the system enters the IRRIGATING state. The relay is activated, opening the solenoid valve and allowing water to flow. Simultaneously, the LED turns ON to indicate active irrigation. Once the soil becomes sufficiently wet, the relay and LED are turned OFF and the system enters a COOLDOWN state before returning to IDLE. If the DHT22 sensor fails three consecutive times, the system enters the FAULT state and irrigation is disabled.

## State Machine

IDLE – Monitors sensor values.
IRRIGATING – Relay and valve are activated, LED turns ON.
COOLDOWN – Prevents rapid switching after irrigation.
FAULT – Triggered when DHT22 readings fail three consecutive times.

## Features

* Automatic irrigation based on soil moisture.
* Temperature and humidity monitoring using DHT22.
* State machine implementation for reliable operation.
* Relay-controlled solenoid valve.
* LED indication during irrigation.
* Fault detection for sensor failures.
* Cooldown mechanism to prevent frequent switching.

## Output

* Displays soil moisture status (DRY/WET).
* Shows temperature and humidity readings on the Serial Monitor.
* Indicates the current state of the system.
* Automatically controls irrigation based on soil conditions.
