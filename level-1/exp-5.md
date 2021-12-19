# Experiment 5 - Buzzer

> An experiment to understand the working of a buzzer.
  
### Components Required 

* Arduino Uno
* Buzzer*1
* Breadboard*1
* Breadboard Jumper Wire*2
* USB cable*1

### Circuit Diagram

![image](https://user-images.githubusercontent.com/51323070/146686768-1a715fea-d535-47cb-a09b-e8d34efdacde.png)

![image](https://user-images.githubusercontent.com/51323070/146686777-21adf3c5-879a-4e89-87f6-4e7a1e0114e4.png)

### Code

```ino
int ledpin=11;// initialize pin 11
int inpin=7;// initialize pin 7
int val;// define val
void setup()
{
pinMode(ledpin,OUTPUT);// set LED pin as “output”
pinMode(inpin,INPUT);// set button pin as “input”
}
void loop()
{
val=digitalRead(inpin);// read the level value of pin 7 and assign if to val
if(val==LOW)// check if the button is pressed, if yes, turn on the LED
{ digitalWrite(ledpin,LOW);}
else
{ digitalWrite(ledpin,HIGH);}
}
```

### Output

> The Buzzer makes beep sound.

![loading](https://user-images.githubusercontent.com/51323070/146673156-df307713-2ec1-46dd-9e6f-5bd0c7afc81f.gif)