# Experiment 4 - Button Controlled LED

> An experiment to trun on LED using a Push Button.
  
### Components Required 

* Arduino Uno
* Button switch*1
* Red M5 LED*1
* 220ΩResistor*1
* 10KΩ Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*6
* USB cable*1

### Circuit Diagram

![image](https://user-images.githubusercontent.com/51323070/146686317-34a081c2-acfb-407c-ab93-999d4f430e08.png)

![image](https://user-images.githubusercontent.com/51323070/146686333-26843fc7-d2bd-46c6-b2ec-980fc071d3dc.png)

![image](https://user-images.githubusercontent.com/51323070/146686337-acbb55ca-aeed-4e5e-9380-dd3b666b28e9.png)

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

> When the push button is pressed the LED is turns on otherwise it is off.

![loading](https://user-images.githubusercontent.com/51323070/146673156-df307713-2ec1-46dd-9e6f-5bd0c7afc81f.gif)