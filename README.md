# ex2-iot
#include <Servo.h>
const int irSensor = 2;
const int servoPin = 9;
Servo myServo;

void setup() {
  pinMode(irSensor, INPUT);
  myServo.attach(servoPin);
  myServo.write(0);
}

void loop() {
  if (digitalRead(irSensor) == LOW) {
    myServo.write(90);
  } else {
    myServo.write(0);
  }
  delay(200);
}
