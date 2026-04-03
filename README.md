# Arduino Sequential Seven-Segment Display Control
## Overview

This project is an Arduino-based embedded system that controls a single-digit seven-segment display. The program sequentially turns ON each segment one by one starting from all segments in the OFF state. After all seven segments are turned ON, the program reverses the sequence by turning OFF each segment one by one until all segments are OFF again. This sequence repeats continuously.

## Description

In this project, the Arduino board is used to control each segment of the seven-segment display through digital output pins. Each segment is activated with a fixed delay so that the segments glow one after another in a sequence. Once all segments are turned ON, the program reverses the order and turns the segments OFF sequentially. This creates a forward and reverse lighting pattern.

## Objective

The objective of this project is to understand how to interface a seven-segment display with Arduino and control individual segments using embedded programming. This project also helps in learning digital output control, looping structures, timing delays, and sequential control logic in embedded systems.

## Working Principle

The Arduino sends digital signals to each segment of the display. The segments are turned ON sequentially with a predefined delay. After all segments are ON, the Arduino turns OFF the segments sequentially in reverse order. This process continues in a loop, creating a continuous ON and OFF sequence pattern.
## Code for Execution

The following Arduino code is used to control the sequential ON and OFF operation of the seven-segment display segments.
```
int pins[] = {2, 3, 4, 5, 6, 7, 8};

void setup() {
  for (int i = 0; i < 7; i++) {
    pinMode(pins[i], OUTPUT);
    digitalWrite(pins[i], LOW); 
  }
}

void loop() {
  for (int i = 0; i < 7; i++) {
    digitalWrite(pins[i], HIGH);
    if (i >= 5) {
      delay(200); 
    } else {
      delay(1000);
    }
  }

  for (int i = 6; i >= 0; i--) {
    digitalWrite(pins[i], LOW);
    if (i >= 5) {
      delay(200);
    } else {
      delay(1000);
    }
  }
}
```

## Output Video Link:
You can view the project output in the following link:

https://videotourl.com/videos/1775221546566-7f1b6d13-dbc1-485f-80f3-deea03abd732.mp4

## Applications

This project can be used in LED pattern generation, display control systems, embedded system experiments, and basic lighting sequence applications using microcontrollers.

## Conclusion

This project demonstrates the sequential ON and OFF control of a seven-segment display using Arduino. It helps beginners understand Arduino programming, hardware interfacing, timing delays, and sequential control in embedded systems.
