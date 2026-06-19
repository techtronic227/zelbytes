# Software Requirements and Libraries

## Software Requirements

* Arduino IDE 2.x or later
* ESP32 Board Package
* Python 3.x
* Command Prompt / Terminal
* WiFi Connection
* Zelbytes IoT Dashboard Account

## Arduino Board Package

Install the following board package through **Boards Manager**:

* **esp32 by Espressif Systems**

Board Selection:

```text
Tools → Board → ESP32 Arduino → ESP32 Dev Module
```

## Arduino Libraries

The following libraries are required:

| Library      | Purpose                                 |
| ------------ | --------------------------------------- |
| WiFi.h       | WiFi connectivity                       |
| HTTPClient.h | HTTP POST requests for telemetry upload |
| WebServer.h  | Local web server for relay control      |

These libraries are included with the ESP32 board package and do not require separate installation.

## Python Packages

Install the following packages:

### PySerial

Used for serial communication between ESP32 and Python.

py -m pip install pyserial
```

### Requests

Used to send telemetry data to the Zelbytes IoT platform.

py -m pip install requests
```

## Hardware Requirements

* ESP32 Development Board
* Soil Moisture Sensor
* Relay Module
* Water Pump
* Push Button
* LED
* 220 Ω Resistor
* Jumper Wires
* Breadboard
* USB Cable
* External Power Supply

## Additional Requirements

* Stable WiFi connection
* USB drivers for ESP32
* Correct COM port selection
* API key for Zelbytes IoT Dashboard
