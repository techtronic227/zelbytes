# FINAL REPORT

# Automated Grow-Bench Prototype

## 1. Introduction

The Automated Grow-Bench Prototype is a smart irrigation system developed using Arduino Uno. The system monitors soil moisture continuously and automatically controls irrigation through a relay-operated pump or solenoid valve. Manual override functionality and serial commands provide additional user control. The project demonstrates the application of embedded systems in precision agriculture and efficient water management.

---

## 2. Hardware Bill of Materials

| Component                 | Quantity | Function                     |
| ------------------------- | -------- | ---------------------------- |
| Arduino Uno               | 1        | Main controller              |
| Soil Moisture Sensor      | 1        | Measures soil moisture level |
| Relay Module              | 1        | Controls the pump or valve   |
| Push Button               | 1        | Enables manual override      |
| Water Pump/Solenoid Valve | 1        | Performs irrigation          |
| Breadboard                | 1        | Circuit assembly             |
| Jumper Wires              | Several  | Connections                  |
| USB Cable                 | 1        | Programming and power        |
| External Power Supply     | 1        | Powers the pump              |

---

## 3. Wiring Diagram

### Pin Connections

| Component       | Arduino Uno Pin |
| --------------- | --------------- |
| Soil Sensor AO  | A0              |
| Relay IN        | D7              |
| Push Button     | D2              |
| Relay VCC       | 5V              |
| Relay GND       | GND             |
| Soil Sensor VCC | 5V              |
| Soil Sensor GND | GND             |

### Images

Include:

* Bench setup photograph
* Circuit diagram
* Fritzing export

Example:

```markdown
![Circuit Diagram](images/circuit.png)

![Bench Setup](images/bench_photo.jpg)
```

---

## 4. Calibration Methodology

The soil moisture sensor was calibrated by measuring readings under dry and wet conditions.

### Dry Soil

Typical values:

600–900

### Wet Soil

Typical values:

200–500

Based on experimental observations, a threshold value of 600 was selected. Values above the threshold indicate dry soil and trigger irrigation, while values below the threshold stop irrigation.

---

## 5. System Working

The soil moisture sensor continuously provides analog readings to the Arduino Uno through pin A0. When the soil becomes dry, the controller activates the relay connected to pin D7, turning on the pump. Once sufficient moisture is restored, irrigation is stopped automatically.

A push button connected to D2 allows switching between automatic and manual modes. Serial commands are also implemented to provide monitoring and control.

Supported commands:

* STATUS
* FORCE_ON
* FORCE_OFF

The system maintains reliable operation through continuous monitoring and user intervention when required.

---

## 6. Test Results

| Test Case             | Result |
| --------------------- | ------ |
| Soil moisture reading | Passed |
| Automatic irrigation  | Passed |
| Relay switching       | Passed |
| Pump operation        | Passed |
| Manual override       | Passed |
| STATUS command        | Passed |
| FORCE_ON command      | Passed |
| FORCE_OFF command     | Passed |

The system successfully responded to both automatic and manual control conditions.

---

## 7. Known Limitations

* Sensor readings depend on soil type and moisture distribution.
* Corrosion of sensor probes may affect long-term accuracy.
* Threshold values may require recalibration.
* Only a single moisture sensing point is used.
* External power supply is required for the pump.

---

## 8. Reflashing Instructions

### Step 1

Install Arduino IDE.

### Step 2

Open:

```text
grow_bench_automation.ino
```

### Step 3

Connect Arduino Uno using a USB cable.

### Step 4

Select:

Tools → Board → Arduino Uno

### Step 5

Choose the appropriate COM port.

### Step 6

Upload the sketch.

### Step 7

Open Serial Monitor.

Set baud rate to:

```text
9600
```

### Step 8

Verify operation using:

```text
STATUS
FORCE_ON
FORCE_OFF
```

---

## 9. Folder Structure

```text
grow_bench_project
│
├── grow_bench_automation.ino
├── README.md
├── docs
│   ├── FINAL_REPORT.md
│   ├── wiring
│   └── images
│       ├── bench_photo.jpg
│       └── circuit.png
```

---

## 10. Conclusion

The Automated Grow-Bench Prototype successfully integrates soil moisture sensing, automatic irrigation, manual override, and serial communication into a single Arduino Uno-based system. The project provides an efficient and reliable solution for smart irrigation and demonstrates the practical implementation of embedded systems in agricultural automation. The modular design allows future enhancements such as cloud connectivity, multiple sensors, and advanced monitoring capabilities.
