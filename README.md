# task1ELEC-WEEK2-
^^ Connect and program an electronic circuit containing 6 servo motors using simulation software.
<br><br> 
This project demonstrates how to control six servo motors using an Arduino board. The simulation is created using Tinkercad, a powerful online tool for creating and testing Arduino circuits. 
<br>

## Requirements

- Tinkercad account
- Arduino Uno
- 6 Servo Motors
- Breadboard
- Jumper Wires

<br>

<img src=https://github.com/user-attachments/assets/7aee05f2-ce18-4161-9db0-74caa5994441 width=80%>

## Circuit Design

1. **Power Connections:** 
   - Connect the VCC (red wire) of all six servo motors to the 5V pin on the Arduino.
   - Connect the GND (black wire) of all six servo motors to the GND pin on the Arduino.
    <br>

    ```bash
    Here is a visual representation of the wiring:

    - Red Wires: Connect to the 5V power supply (Arduino 5V pin).
    - Black Wires: Connect to the ground (Arduino GND pin).
    - Green Wires: Connect to the corresponding digital pins on the Arduino for each servo motor.
    ```

2. **Signal Connections:**
   - Connect the signal (control) wire of each servo motor to the following Arduino digital pins:
     - Servo 1: Digital Pin 9
     - Servo 2: Digital Pin 8
     - Servo 3: Digital Pin 7
     - Servo 4: Digital Pin 6
     - Servo 5: Digital Pin 5
     - Servo 6: Digital Pin 4
    
## Arduino Code

```bash

#include <Servo.h>

Servo s1;
Servo s2;
Servo s3;
Servo s4;
Servo s5;
Servo s6;

void setup() {
    s1.attach(4); //attaches the servo on pin 8 to the servo object
    s2.attach(5);
    s3.attach(6);
    s4.attach(7);
    s5.attach(8);
    s6.attach(9);
}

void loop() {
  
  // Move all servos to 0 degrees
  s1.write(0);
  s2.write(0);
  s3.write(0);
  s4.write(0);
  s5.write(0);
  s6.write(0);
  delay(1000); // Wait for 1 second

  // Move all servos to 90 degrees
  s1.write(90);
  s2.write(90);
  s3.write(90);
  s4.write(90);
  s5.write(90);
  s6.write(90);
  delay(1000); // Wait for 1 second

  // Move all servos to 180 degrees
  s1.write(180);
  s2.write(180);
  s3.write(180);
  s4.write(180);
  s5.write(180);
  s6.write(180);
  delay(1000); // Wait for 1 second

  // Move servos to random positions
  s1.write(random(0, 181));
  s2.write(random(0, 181));
  s3.write(random(0, 181));
  s4.write(random(0, 181));
  s5.write(random(0, 181));
  s6.write(random(0, 181));
  delay(1000); // Wait for 1 second

}
```
<br>

^^ Here is the link for my Circuit : https://www.tinkercad.com/things/cJMtvMdVoNj-smooth-gogo
