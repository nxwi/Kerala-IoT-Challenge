# Experiment 1 - Hello World LED Blinking

> A basic Program similar to printing "*Hello World* " in any programming language. The Aim is to blink an LED using **Arduino Uno Board**.
> Arduino Uno is an open-source microcontroller board developed by Arduino.cc. It has several advantages over conventional microcontrollers. It comes with pre-tested software and hardware libraries and has its own integrated development environment (IDE). Also, it is less expensive & beginner-friendly.
### Components Required 

* Arduino Uno Board
* USB Cable
* LED (Any Color) x 1 Nos
* 220 OHM Resistor X 1 Nos
* Breadboard
* Jumper Wires (Male to Male ) X 2 Nos

### Circuit Diagram

![image](https://user-images.githubusercontent.com/51323070/146635167-1adbc624-0140-444f-b14c-eb33bedc723f.png)

### Code

```ino
int ledPin = 10; // define digital pin 10.
void setup()
{
pinMode(ledPin, OUTPUT);// define pin with LED connected as output.
}
void loop()
{
digitalWrite(ledPin, HIGH); // set the LED on.
delay(1000); // wait for a second.
digitalWrite(ledPin, LOW); // set the LED off.
delay(1000); // wait for a second
}
```

### Output

> The LED blinked with a time interval of 1 second.
![]()