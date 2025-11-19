# Arduino Ultrasonic Alarm Meter

This is a simple Arduino project that uses an **HC-SR04 ultrasonic sensor** and a **buzzer** to create a distance-based alarm system.

- When an object comes within 50 cm of the sensor, the buzzer activates. 
- The closer the object, the faster the buzzer beeps.

---

## Hardware Components

- Arduino Uno / Nano
- HC-SR04 Ultrasonic Sensor
- Active Buzzer
- Jumper Wires

---

## Wiring

**HC-SR04 → Arduino**

| HC-SR04 | Arduino |
|---------|---------|
| VCC     | 5V      |
| GND     | GND     |
| TRIG    | D6      |
| ECHO    | D5      |

**Buzzer → Arduino**

| Buzzer | Arduino |
|--------|---------|
| +      | D2      |
| -      | GND     |

---

## How It Works

1. The Arduino triggers the ultrasonic sensor to send a pulse.
2. The sensor measures the time for the pulse to return.
3. The distance is calculated using the formula: 
   `distance = (duration / 2) / 29.1` cm
4. If the object is closer than 50 cm, the buzzer turns on. 
   - The closer the object, the shorter the buzzer delay, resulting in faster beeps.
5. The distance is also printed to the Serial Monitor for debugging.

---
