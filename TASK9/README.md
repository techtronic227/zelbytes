# Automated Grow-Bench Prototype

## Overview

The Automated Grow-Bench Prototype is an ESP8266-based smart irrigation system designed to automate plant watering using soil moisture measurements. The system continuously monitors the moisture level of the soil and automatically activates a relay-controlled water valve or pump when the soil becomes dry. Irrigation stops once adequate moisture is restored, ensuring efficient water usage.

The prototype supports both automatic and manual operation. A push button provides manual override, allowing the user to directly control the valve, while serial commands (`STATUS`, `FORCE_ON`, `FORCE_OFF`, and `AUTO`) enable monitoring and control through the Serial Monitor. Separate dry and wet thresholds are used to implement hysteresis and prevent frequent relay switching.

This project integrates sensor monitoring, relay control, manual override, and serial communication into a single firmware, providing a reliable and user-friendly smart irrigation solution suitable for capstone evaluation and future IoT-based grow-bench applications.
