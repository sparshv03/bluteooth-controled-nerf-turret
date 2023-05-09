#include <Servo.h>
Servo s;

void setup() {
  s.attach(7);
}

void loop() {
  s.write(60);
  delay(2000);
  s.write(180);
  delay(400);
}


#define ledPin 7
int state = 0;

void setup() {
  pinMode(ledPin, OUTPUT);
  digitalWrite(ledPin, LOW);
  Serial.begin(38400); // Default communication rate of the Bluetooth module
}

void loop() {
  if(Serial.available() > 0){ // Checks whether data is comming from the serial port
    state = Serial.read(); // Reads the data from the serial port
 }

 if (state == '0') {
  digitalWrite(ledPin, LOW); // Turn LED OFF
  Serial.println("LED: OFF"); // Send back, to the phone, the String "LED: ON"
  state = 0;
 }
 else if (state == '1') {
  digitalWrite(ledPin, HIGH);
  Serial.println("LED: ON");;
  state = 0;
 } 
}
