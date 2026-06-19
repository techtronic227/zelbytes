## HC-SR04 Ultrasonic Sensor

### Features

* Measures distance using **ultrasonic sound waves (40 kHz)**.
* Operating voltage: **5V DC**.
* Measuring range: **2 cm to 400 cm**.
* Accuracy: approximately **±3 mm**.
* Consists of **one transmitter** and **one receiver** transducer.
* Provides non-contact distance measurement.

### Working

1. The Arduino sends a **10 µs pulse** to the **TRIG** pin.
2. The sensor transmits an ultrasonic wave through the transmitter.
3. The wave travels through the air and reflects from an object.
4. The receiver detects the reflected wave.
5. The sensor outputs a pulse on the **ECHO** pin whose duration corresponds to the travel time of the sound wave.
6. The Arduino calculates the distance using the measured time and the speed of sound.
