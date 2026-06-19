# Motor and Valve Control System with Emergency Stop

This project implements a motor and valve control system using an Arduino Uno, L298N motor driver, relay module, and an emergency stop button. The system allows independent control of the DC motor and solenoid valve through serial commands.

The Arduino Uno acts as the main controller and communicates with the L298N motor driver to regulate the speed and direction of the DC motor using PWM signals. A relay module is used to operate the solenoid valve independently, allowing fluid flow to be controlled without affecting the motor operation. An LED connected to the Arduino provides a visual indication of the motor status by blinking while the motor is running.

An emergency stop button is implemented using an interrupt on pin 2. When pressed, the system immediately stops the motor, closes the valve, and enters a safe state. Normal operation can be restored only after sending a reset command through the Serial Monitor.

NOTE: No flyback diode was used in the current implementation.