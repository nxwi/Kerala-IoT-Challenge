# Experiment 11 - Potentiometer analog Value Reading

> An experiment to understand the working of Potentiometer.

### Components Required

* Arduino Uno Board*1
* 10K Potentiometer *1
* Breadboard*1
* Breadboard Jumper Wire*3
* USB cable*1

### Circuit Diagrams

![image](https://user-images.githubusercontent.com/51323070/146688004-adc8a647-9be8-42b0-8256-98a63afd6b51.png)

![image](https://user-images.githubusercontent.com/51323070/146688007-13745dcc-2c62-4228-b4ad-2c7507c10feb.png)

### Code

```ino
int potpin=0;// initialize analog pin 0
int ledpin=13;// initialize digital pin 13
int val=0;// define val, assign initial value 0
void setup()
{
pinMode(ledpin,OUTPUT);// set digital pin as “output”
Serial.begin(9600);// set baud rate at 9600
}
void loop()
{
digitalWrite(ledpin,HIGH);// turn on the LED on pin 13
delay(50);// wait for 0.05 second
digitalWrite(ledpin,LOW);// turn off the LED on pin 13
delay(50);// wait for 0.05 second
val=analogRead(potpin);// read the analog value of analog pin 0, and assign it to val 
Serial.println(val);// display val’s value
}
```

### Output

![loading](https://user-images.githubusercontent.com/51323070/146673156-df307713-2ec1-46dd-9e6f-5bd0c7afc81f.gif)
