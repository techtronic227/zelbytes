## Hardware Used

1.Arduino Uno

Use:Acts as the main controller of the system.

Working:The Arduino reads the analog voltage from the LDR through pin A0, converts it into a digital value (0–1023) using its built-in ADC, and displays the readings on the Serial Monitor.


2.LDR (Light Dependent Resistor)

Use:Detects the intensity of light in the surroundings.

Working:The resistance of the LDR changes according to the amount of light falling on it. In bright light its resistance decreases, while in darkness its resistance increases. This change is used to measure light levels.



3.10 kΩ Resistor

Use:Forms a voltage divider with the LDR.

Working:The resistor works together with the LDR to generate a variable voltage that depends on light intensity. This voltage is fed to the Arduino's analog input for measurement.



