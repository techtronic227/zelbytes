Relay and Solenoid Valve Working

1. Initially, the relay is in the OFF state, so the solenoid valve does not receive power. The valve remains closed, preventing water flow through the irrigation system.

2. When the manual button is pressed, the Arduino detects the input and immediately sends a control signal to the relay module. The relay coil is energized, causing the relay contacts to switch.

3. Within a few milliseconds, the relay connects the external power supply to the solenoid valve. The valve coil becomes energized and generates a magnetic field.

4. The magnetic field lifts the valve plunger, opening the valve and allowing water to flow through the irrigation pipeline. At the same time, the Arduino starts a timer.

5. The valve remains open for **5 seconds**, during which water is supplied to the plants. The relay stays energized throughout this period to maintain power to the valve.

6. After the 5-second delay has elapsed, the Arduino automatically sends a LOW signal to the relay input. The relay coil is de-energized, and the contacts return to their normal position.

7. Power to the solenoid valve is disconnected, causing the magnetic field inside the valve to collapse. The internal spring pushes the plunger back to its original position.

8. The valve closes, stopping the water flow completely. The relay remains OFF until the button is pressed again, ensuring controlled and timed irrigation without continuous operation.

9. This automatic shutoff mechanism prevents unnecessary water usage, protects the valve from prolonged energization, and improves the efficiency of the irrigation system.
