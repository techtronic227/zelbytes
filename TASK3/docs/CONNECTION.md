### Connection Manual

#### 1. Push Button

| Push Button Pin   | Arduino Nano |
| ----------------- | ------------ |
| One terminal      | D2           |
| Opposite terminal | GND          |


#### 2. Relay Module

| Relay Pin | Arduino Nano |
| --------- | ------------ |
| VCC       | 5V           |
| GND       | GND          |
| IN        | D8           |


#### 3. LED

| LED Component | Arduino Nano               |
| ------------- | -------------------------- |
| Anode (+)     | D13 through 220 Ω resistor |
| Cathode (-)   | GND                        |



### Complete Wiring Summary

| Arduino Pin | Connected To                   |
| ----------- | ------------------------------ |
| D2          | Push Button                    |
| D8          | Relay IN                       |
| D13         | LED (+) through 220 Ω resistor |
| 5V          | Relay VCC                      |
| GND         | Relay GND, Button GND, LED GND |


When the button is pressed, Arduino activates the relay through D8, the relay powers the solenoid valve, and water flows. The LED connected to D13 turns ON to indicate that irrigation is active.
