### 1. Arduino Uno

**Hardware Details**

* Based on ATmega328P microcontroller.
* Operating voltage: 5V.
* 14 Digital I/O pins and 6 Analog input pins.
* USB interface for programming and power supply.
* Clock speed: 16 MHz.

**Working**
Arduino Uno acts as the main controller of the system. It reads the analog value from the soil moisture sensor through pin A0, processes the data, and can make decisions such as turning irrigation devices ON or OFF based on the moisture level.



### 2. Soil Moisture Sensor (Resistive Type)

**Hardware Details**

* Consists of two conductive probe electrodes.
* Operates with 3.3V–5V supply.
* Measures soil conductivity related to water content.
* Used for detecting dry and wet soil conditions.

**Working**
The probe is inserted into the soil. When soil moisture increases, electrical resistance between the probes decreases. The sensor detects this change and produces a signal corresponding to the moisture level.



### 3. Comparator Module (LM393)

**Hardware Details**

* Uses LM393 voltage comparator IC.
* Provides Analog Output (AO) and Digital Output (DO).
* Includes sensitivity adjustment potentiometer.
* Operates at 3.3V–5V.

**Working**
The module receives the signal from the soil moisture probe and converts it into an analog voltage. The AO pin sends a continuous moisture value to the Arduino, while the DO pin can provide a HIGH or LOW signal based on a preset threshold.


