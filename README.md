# Sound_Sensor_Check

Overview
It is just random thought to check whether the sound sensor working or not 

# check out demo
https://drive.google.com/file/d/1hrtuT4pZKdALKrDZjIC9E1IQZdTzZyHU/view?usp=sharing



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
