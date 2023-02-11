---
layout: essay
type: essay
title: "Corrosion Test - StaySeat"
# All dates must be YYYY-MM-DD format!
date: 2023
published: true
labels:
  - DIY
  - Design
  - R&D
  - Arduino
---

<img class="img-fluid" src="../img/StaySeat/prima.gif">


In this project I helped the StaySeat startup to build something able to perform a dipping corrosion test in saline water for their Copper disks used as magnetic conductive metal for charging purposes.
The different pieces and materials as seen in the gif above have been chosen from the waste pile as the design did not have to be polished.

The Arduino code has been manually written in order to move the motor angle and hence make the samples go up and down.
Here's the very simple code used for the Arduino Mega 2560:

 ```cpp

 // include the Servo library
#include <Servo.h>

Servo myServo;  // create a servo object

 // analog pin used to connect the potentiometer
          // variable to read the value from the analog pin
int angle;              // variable to hold the angle for the servo motor

void setup() {
  myServo.attach(12);   // attaches the servo on pin 12 to the servo object
  Serial.begin(9600);  // open a serial connection to your computer
}

void loop() {

 
  myServo.write(10); //put the motor angle at 10 degrees
  delay(600000); //Wait for 10 minutes


  myServo.write(170); //put the motor angle at 170 degrees
  delay(600000); //Wait for 10 minutes
}

  ```


Here's the final version (without water and sped up for the sake of showing the movement and design alone) with both the copper pieces and references attached at roughly the same lenght


<img class="img-fluid" src="../img/StaySeat/dopo.gif">
