### Hardware Details

#### 1. Arduino Nano

* Microcontroller: ATmega328P
* Operating Voltage: 5V
* Input Voltage: 7V–12V (recommended)
* Digital I/O Pins: 14
* Analog Input Pins: 8
* Clock Speed: 16 MHz
* Flash Memory: 32 KB
* Used to control the relay, monitor the button, and handle serial communication.



#### 2. Push Button

* Type: Momentary Tactile Switch
* Operating Voltage: 5V
* Connected to Digital Pin D2
* Used for manual irrigation control.
* Works with Arduino's internal pull-up resistor.



#### 3. Relay Module

* Type: 1-Channel 5V Relay Module
* Control Voltage: 5V
* Input Signal: Digital Output from Arduino
* Connected to Digital Pin D8
* Provides electrical isolation between Arduino and solenoid valve.
* Used to switch the valve ON and OFF.



#### 4. Solenoid Valve

* Type: Normally Closed (NC) Solenoid Valve
* Operating Voltage: Depends on model (commonly 12V DC)
* Opens when power is supplied through the relay.
* Controls the flow of water for irrigation.



#### 5. Status LED

* Operating Voltage: 2V–3V
* Connected to Digital Pin D13 through a 220 Ω resistor
* Indicates valve status:

  * ON → Valve Open
  * OFF → Valve Closed


#### 6. Current Limiting Resistor

* Resistance: 220 Ω
* Connected in series with the LED
* Limits current to protect the LED and Arduino pin.



#### 7. Breadboard

* Used for temporary circuit assembly.
* Allows easy connection of components without soldering.



#### 8. Power Supply

* Arduino: 5V via USB
* Solenoid Valve: External supply (e.g., 12V DC)
* Provides power required for valve operation.



