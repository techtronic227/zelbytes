# Task 7: CSV Data Logging

## Objective
To collect temperature, humidity, soil moisture, and light intensity data and store them in CSV format for analysis.

## Hardware Used
- Arduino Uno
- DHT22 Sensor
- Soil Moisture Sensor
- LDR
- 10 kΩ Resistor
- Breadboard
- Jumper Wires
- USB Cable

## Connections

### DHT22 Sensor
- VCC → 5V
- DATA → D4
- GND → GND

### Soil Moisture Sensor
- VCC → 5V
- GND → GND
- AO → A0

### LDR
- One leg → 5V
- Other leg → A1 and 10 kΩ resistor
- Other end of resistor → GND

## Software Requirements
- Arduino IDE
- Adafruit DHT Sensor Library

## Procedure

1. Connect all sensors to the Arduino Uno.
2. Open the Arduino IDE and upload `sensor_logger.ino`.
3. Open the Serial Monitor at 9600 baud.
4. The sensor values are displayed in CSV format with the header:

timestamp,temp,humidity,soil,light

5. Collect readings continuously for 30 minutes.
6. Copy and save the data as:

logging_sketch.csv

Example:

logging_sketch.csv

## Working

- The DHT22 sensor measures temperature and humidity.
- The soil moisture sensor measures soil moisture level.
- The LDR measures ambient light intensity.
- Arduino Uno reads all sensor values every 2 seconds.
- The elapsed time is obtained using `millis()`.
- The readings are transmitted through Serial communication in CSV format and stored in a CSV file for analysis.

## Error Handling

- Invalid DHT22 readings (NaN) are skipped.
- Data logging resumes automatically during the next cycle.
- Sensor readings are appended continuously without overwriting previous data.
