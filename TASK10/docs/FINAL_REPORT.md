# **Final Firmware Report – Smart Soil Moisture Monitoring and Automatic Irrigation System**

## **Student Information**

**Name:** Mridula A Chandran

**College:** Sree Chitra Thirunal College of Engineering

**Branch:** Electronics and Communication Engineering

**Internship:** Zelbytes Arduino Foundations Internship

---

# **1. Project Overview**

The Smart Soil Moisture Monitoring and Automatic Irrigation System is an IoT-based solution developed using an ESP32, soil moisture sensor, relay module, and WiFi connectivity. The system continuously monitors soil conditions and automatically controls irrigation based on moisture levels.

## Objectives

* Monitor soil moisture in real time.
* Automate irrigation.
* Support manual override.
* Upload telemetry data to the Zelbytes IoT Dashboard.
* Provide remote monitoring capabilities.

## Key Features

* Automatic irrigation control
* Manual relay override
* Serial command interface
* WiFi connectivity
* Cloud telemetry integration
* Dashboard visualization

---

# **2. System Architecture**

The system consists of sensing, control, communication, and actuation layers.

## Sensor Layer

The soil moisture sensor measures soil conditions and provides analog readings to the ESP32.

## Controller Layer

The ESP32 processes sensor readings and determines whether irrigation is required.

## Communication Layer

WiFi connectivity enables telemetry upload to the Zelbytes IoT platform.

## Actuator Layer

A relay module controls the water pump according to soil conditions.

---

# **3. Hardware Bill of Materials**

| Component            | Quantity | Purpose           |
| -------------------- | -------- | ----------------- |
| ESP32                | 1        | Main Controller   |
| Soil Moisture Sensor | 1        | Soil Monitoring   |
| Relay Module         | 1        | Pump Control      |
| Push Button          | 1        | Manual Override   |
| LED                  | 1        | Status Indication |
| Jumper Wires         | Several  | Connections       |
| USB Cable            | 1        | Programming       |

---

# **4. Wiring Connections**

| Component               | ESP32 Pin |
| ----------------------- | --------- |
| Soil Moisture Sensor A0 | GPIO34    |
| Relay Module IN         | GPIO26    |
| Push Button             | GPIO27    |
| LED                     | GPIO2     |

All modules share a common ground connection.

---

# **5. Firmware Design**

## Automatic Irrigation Logic

The ESP32 continuously reads soil moisture values.

* Dry soil → Relay ON → Pump ON
* Wet soil → Relay OFF → Pump OFF

## Manual Override

Manual control is provided using:

* Push button
* Serial commands

## Serial Commands

* STATUS
* FORCE_ON
* FORCE_OFF

## Telemetry Upload

Sensor values are uploaded to the Zelbytes IoT Dashboard through HTTP POST requests.

---

# **6. Sensor Calibration Methodology**

## Dry Soil

Typical ADC values:

* 2800 – 3500

## Wet Soil

Typical ADC values:

* 800 – 1500

## Selected Threshold

Threshold value:

* 2000 ADC

---

# **7. Dashboard Integration**

The dashboard provides:

* Soil moisture percentage
* Historical data visualization
* Real-time monitoring

---

# **8. Testing Procedure**

### Test Case 1

Dry soil condition.

Expected Result:

Pump ON

Result: PASS

### Test Case 2

Wet soil condition.

Expected Result:

Pump OFF

Result: PASS

### Test Case 3

Manual override using push button.

Expected Result:

Relay toggles

Result: PASS

### Test Case 4

Telemetry upload.

Expected Result:

Dashboard receives data

Result: PASS

---

# **9. Test Results Summary**

| Test Item        | Result |
| ---------------- | ------ |
| Sensor Reading   | PASS   |
| Auto Irrigation  | PASS   |
| Relay Operation  | PASS   |
| WiFi Connection  | PASS   |
| Telemetry Upload | PASS   |
| Manual Override  | PASS   |
| Serial Commands  | PASS   |

---

# **10. Known Limitations**

1. Single sensor support.
2. WiFi dependency.
3. No battery backup.
4. No weather prediction support.

---

# **11. Reflash Instructions for Next Intern**

1. Install Arduino IDE.
2. Install ESP32 board package.
3. Open the firmware source code.
4. Update WiFi credentials.
5. Select the appropriate COM port.
6. Upload the firmware.
7. Verify operation using Serial Monitor.

---

# **12. Future Improvements**

* Multiple sensor support
* Mobile application
* Solar-powered operation
* MQTT communication
* Weather-based irrigation scheduling

---

# **13. Conclusion**

The Smart Soil Moisture Monitoring and Automatic Irrigation System successfully demonstrates automated irrigation using ESP32 and IoT technologies. The system integrates sensing, control, WiFi communication, and dashboard monitoring to provide an efficient and reliable solution for smart agriculture applications.
