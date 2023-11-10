# Sound_Sensor_Check

# Overview
https://github.com/RawHit02/Radar_System-IOT-/assets/107709247/2763e295-169b-4f15-b7e8-b06037a81043

# check out demo
https://drive.google.com/file/d/1hrtuT4pZKdALKrDZjIC9E1IQZdTzZyHU/view?usp=sharing

![image](https://github.com/RawHit02/Sound_Sensor_Check/assets/107709247/c4af19f7-8039-4468-9022-556e7f5e6c06)
![image](https://github.com/RawHit02/Sound_Sensor_Check/assets/107709247/fc1cba1b-f54b-42fd-af5e-763b2878cba7)
![image](https://github.com/RawHit02/Sound_Sensor_Check/assets/107709247/190c761c-bd83-4092-b74b-1f8de0d17cdf)



# Hardware Components
Arduino Uno
Sound Sensor
Jumper Wires
Other components...
Software Requirements

  
# c++ Code
int sensor = 2; // Connected to digital output of KY-038 sound sensor module
int led = 13; // Connected to postive of led
boolean is_on = false; //To determine/track if led is on or off
void setup() {
  pinMode(sensor, INPUT); //Setting the pin to input for reading data
  pinMode(led, OUTPUT); //Setting the pin to output for turning the led on/off

}
void loop() {
  int data = digitalRead(sensor); //Reading data from sensor and storing in variable

  if (data == 1) { // 1 is sent from sensor when loud noise is detected
    if (is_on == true) { // If led is on then turn it off
      digitalWrite(led, LOW);
      is_on = false;
    }
    else { // else if led is off then turn it on
      digitalWrite(led, HIGH);
      is_on = true;
    }
  }
}

# Fork the repository
Create a new branch (git checkout -b feature)
Make your changes
Commit your changes (git commit -m 'Add feature')
Push to the branch (git push origin feature)
Create a pull request
