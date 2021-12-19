# Experiment 6 - RGB LED

> An experiment to understand the working of a RGB LED.
  
### Components Required 

* Arduino Uno
* USB Cable * 1
* RGB LED * 1
* Resistor *3
* Breadboard jumper wire*5

### Circuit Diagram

![image](https://user-images.githubusercontent.com/51323070/146686878-47ef7f36-e76d-4241-92df-6b5ccc3856c7.png)

![image](https://user-images.githubusercontent.com/51323070/146686880-383a3ea4-bc3f-41fe-b9c1-ada4b3ba82e0.png)

### Code

```ino
int redpin = 11; //select the pin for the red LED
int bluepin =10; // select the pin for the blue LED
int greenpin =9;// select the pin for the green LED
int val;
void setup() {
  pinMode(redpin, OUTPUT);
  pinMode(bluepin, OUTPUT);
  pinMode(greenpin, OUTPUT);
  Serial.begin(9600);
}
void loop() 
{
for(val=255; val>0; val--)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
for(val=0; val<255; val++)
  {
   analogWrite(11, val);
   analogWrite(10, 255-val);
   analogWrite(9, 128-val);
   delay(1); 
  }
 Serial.println(val, DEC);
}
}
```

### Output

> The RGB LED blinks.

![loading](https://user-images.githubusercontent.com/51323070/146673156-df307713-2ec1-46dd-9e6f-5bd0c7afc81f.gif)
