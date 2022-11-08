# Animating-a-servo-with-a-potentiometer

#include <Servo.h>
 
Servo cntServo1; 
int spin1 = 2;
int lightValue1; 
 
int sensorPin1 = A0; 
 
int potPin1 = A1;
int potValue1; 
 
int controlServo; 
 
void setup() {
 // put your setup code here, to run once:
 
cntServo1.attach(spin1);
  
}
 
void loop() {
 
potValue1 = analogRead(potPin1);
 
 
// Code to control servo using pot1
 
controlServo = map(analogRead(A1),0,1023,0,180); // map potPin1 to cntServo1 values
 
 cntServo1.write(controlServo);
 
}
