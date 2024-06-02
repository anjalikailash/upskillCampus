# upskillCampus
In this home automation project, we are creating a simple system using an Arduino to control a few devices (LED and Bulb) and monitor environmental parameters (motion, distance, and temperature). Below is an explanation of how each component is connected and functions within the circuit:
Components:
1.	Arduino
2.	LED
3.	Bulb
4.	Resistor
5.	PIR Sensor (Passive Infrared Sensor)
6.	Breadboard (Small)
7.	Ultrasonic Distance Sensor
8.	Temperature Sensor
Circuit Design:
Arduino:
•	Acts as the central controller, processing inputs from sensors and controlling outputs like LEDs and bulbs.
LED:
•	Connected to a digital pin on the Arduino, controlled to indicate status or events (e.g., motion detected).
Bulb:
•	Connected through a relay module to handle high voltage. The relay is controlled by a digital pin on the Arduino to switch the bulb on/off.
Resistor:
•	Used to limit current to the LED, typically a 220-ohm resistor is used in series with the LED.
PIR Sensor:
•	Detects motion within its range. When motion is detected, it sends a HIGH signal to the Arduino.
•	Connected to a digital input pin on the Arduino.
Breadboard (Small):
•	Provides a platform for assembling the circuit, making it easier to connect components without soldering.
Ultrasonic Distance Sensor:
•	Measures the distance to an object using sound waves.
•	The Trigger pin is connected to a digital output pin, and the Echo pin is connected to a digital input pin on the Arduino.
Temperature Sensor:
•	Measures the ambient temperature.
•	Connected to an analog input pin on the Arduino.
Wiring Connections:
1.	LED:
•	Cathode (short leg): Connected to GND.
•	Anode (long leg): Connected to a digital pin on the Arduino through a 220-ohm resistor.
2.	Bulb:
•	Connected to the relay module.
•	Relay Input: Connected to a digital pin on the Arduino.
•	Relay Output: One side to the high voltage AC supply, the other side to the bulb.
3.	PIR Sensor:
•	VCC: Connected to 5V on the Arduino.
•	GND: Connected to GND on the Arduino.
•	OUT: Connected to a digital input pin on the Arduino.
4.	Ultrasonic Distance Sensor:
•	VCC: Connected to 5V on the Arduino.
•	GND: Connected to GND on the Arduino.
•	Trig: Connected to a digital output pin on the Arduino.
•	Echo: Connected to a digital input pin on the Arduino.
5.	Temperature Sensor:
•	VCC: Connected to 5V on the Arduino.
•	GND: Connected to GND on the Arduino.
•	Analog Output: Connected to an analog input pin on the Arduino.

Code Explanation:
The Arduino code will include libraries and setup for each sensor and component. The loop function will constantly check sensor inputs and control the outputs accordingly. Here’s a simple outline of the code logic:
1.	Setup Function:
•	Initialize serial communication for debugging.
•	Set pin modes for all connected components.
2.	Loop Function:
•	PIR Sensor: Check for motion. If motion is detected, turn on the LED and/or bulb.
•	Ultrasonic Sensor: Measure distance. If an object is within a specified range, perform an action (e.g., turn on a light).
•	Temperature Sensor: Read the temperature. If the temperature exceeds a threshold, take appropriate action (e.g., turn on a cooling fan).

