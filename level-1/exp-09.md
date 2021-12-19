# Experiment 9 - LM35 Temperature Sensor

> An experiment to understand the working of an LM35 Temperature Sensor.

### LM35 Temperature Sensor

> LM35 is a common and easy-to-use temperature sensor. LM35 is a widely used temperature sensor with many different package types. At room temperature, it can achieve the accuracy of ±1/4°C without additional calibration processing. LM35 temperature sensor can produce different voltage by different temperature When temperature is 0 ℃, it outputs 0V; if increasing 1 ℃, the output voltage will increase 10 mv.

![image](https://user-images.githubusercontent.com/51323070/146687682-9cf0aad7-b0d7-4c0b-ac4c-c19096aecd0e.png)

### Components Required

* Arduino Uno  Board*1
* LM35*1
* Breadboard*1
* Breadboard Jumper Wire*5
* USB cable*1

### Circuit Diagrams

![image](https://user-images.githubusercontent.com/51323070/146687746-a51bda3c-aa48-43c1-bfd2-c4f426891d67.png)

![image](https://user-images.githubusercontent.com/51323070/146687748-001718ed-d58d-4473-829d-74de902a87b9.png)

### Code

```ino
int potPin = 0; // initialize analog pin 0 for LM35 temperature sensor
void setup()
{
Serial.begin(9600);// set baud rate at”9600”
}
void loop()
{
int val;// define variable
int dat;// define variable
val=analogRead(0);// read the analog value of the sensor and assign it to val
dat=(125*val)>>8;// temperature calculation formula
Serial.print("Tep");// output and display characters beginning with Tep
Serial.print(dat);// output and display value of dat
Serial.println("C");// display “C” characters
delay(500);// wait for 0.5 second
}
```

### Output

![loading](https://user-images.githubusercontent.com/51323070/146673156-df307713-2ec1-46dd-9e6f-5bd0c7afc81f.gif)
