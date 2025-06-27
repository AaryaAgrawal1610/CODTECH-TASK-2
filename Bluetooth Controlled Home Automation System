#include <SoftwareSerial.h>

SoftwareSerial BT(10, 11); // RX, TX for HC-05

int devicePin = 8; // Device control pin

void setup() {
  pinMode(devicePin, OUTPUT);
  BT.begin(9600);   // Start Bluetooth communication
  Serial.begin(9600);
}

void loop() {
  if (BT.available()) {
    char command = BT.read();
    Serial.println(command);
    
    if (command == '1') {
      digitalWrite(devicePin, HIGH); // Turn ON device
    } else if (command == '0') {
      digitalWrite(devicePin, LOW);  // Turn OFF device
    }
  }
}
