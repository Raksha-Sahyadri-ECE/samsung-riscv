**Project Name and Overview**
Project Name:
Random Number Generator Using VSDSQUADRON Mini

Overview:
This project generates and displays a random number on the Serial Monitor using the VSDSQUADRON Mini board. The random numbers range from 1 to 6, simulating the roll of a dice. 

**Components Required:**
VSDSQUADRON Mini (CH32) Board
USB Type-C Cable (for power and data communication)

**Pinout Diagram:**
No external connections are required, as the random number is generated internally and displayed on the Serial Monitor.

**Code:**
#include <ch32v00x.h>

void setup() {
  Serial.begin(115200);             // Initialize Serial Communication at 115200 baud rate
  randomSeed(analogRead(A0));       // Seed the random number generator using a floating analog pin
}

void loop() {
  int randomNumber = random(1, 7);  // Generate a random number between 1 and 6
  Serial.println(randomNumber);     // Print the number to the Serial Monitor
  delay(1000);                      // Wait for a second before generating the next number
}
