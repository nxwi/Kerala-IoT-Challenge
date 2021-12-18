# Level 1: Basic Electronics & Arduino

### Basic Electronics, Sensors,Arduino Programming and a Live Project

### Experiment List
Exp No       | List
------------ | -------------
1 |	LED Blinking
2 |	Traffic Light
3 |   LED Chasing
4 |	Button controlled LED
5 |   Buzzer
6 |   RGB LED
7 |   LDR Light sensor
8 |   Flame sensor
9 |   Temperature sensor
10|   IR Remote control
11|	Potentiometer Analog value reading
12|   7 Segment display

<HR>

## Experiment 1 - Hello World LED Blinking

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

<HR>

## Experiment 2 - Traffic Light

> In the previous program, we have done the LED blinking experiment with one LED. Now, it’s time to up the stakes and do a bit more complicated experiment-traffic lights. Actually, these two experiments are similar. While in this traffic lights experiment, we use 3 LEDs with different colors rather than 1 LED.
  
### Components Required 

* Arduino board *1
* USB cable *1
* Red M5 LED*1
* Yellow M5 LED*1
* Green M5 LED*1
* 220Ω resistor *3
* Breadboard*1
* Breadboard jumper wires* several

### Circuit Diagram

![image](https://user-images.githubusercontent.com/51323070/146635146-967f4454-ad07-45b9-94b5-907dca33e3a4.png)

### Code

```ino
int redled =10; // initialize digital pin 8.
int yellowled =7; // initialize digital pin 7.
int greenled =4; // initialize digital pin 4.
void setup()
{
pinMode(redled, OUTPUT);// set the pin with red LED as “output”
pinMode(yellowled, OUTPUT); // set the pin with yellow LED as “output”
pinMode(greenled, OUTPUT); // set the pin with green LED as “output”
}
void loop()
{
digitalWrite(greenled, HIGH);//// turn on green LED
delay(5000);// wait 5 seconds

digitalWrite(greenled, LOW); // turn off green LED
for(int i=0;i<3;i++)// blinks for 3 times
{
delay(500);// wait 0.5 second
digitalWrite(yellowled, HIGH);// turn on yellow LED
delay(500);// wait 0.5 second
digitalWrite(yellowled, LOW);// turn off yellow LED
} 
delay(500);// wait 0.5 second
digitalWrite(redled, HIGH);// turn on red LED
delay(5000);// wait 5 seconds
digitalWrite(redled, LOW);// turn off red LED
}
```

### Output

> In the Traffic light, the green LED blinked for about 5 seconds, then it turned off. Then the yellow LED blinks 3 times with a time interval of 0.5 seconds. Then the red LED blinked for about 5 seconds. This process continues.

![]()

<HR>

## Experiment 3 - LED Chasing Effect

> We often see billboards composed of colourful LEDs. They are constantly changing to form various light effects. In this experiment, we compile a program to simulate the LED chasing effect. The long lead of LED is the positive side; the short lead is negative.
  
### Components Required 

* Led *6
* Arduino board *1
* 220Ω resistor *6
* Breadboard *1
* USB cable*1
* Breadboard wire *13

### Circuit Diagram

![image](https://user-images.githubusercontent.com/51323070/146635338-66471849-2a6e-4570-aaad-508447dc1487.png)

### Code

```ino
int BASE = 2 ;  // the I/O pin for the first LED
int NUM = 6;   // number of LEDs
void setup()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     pinMode(i, OUTPUT);   // set I/O pins as output
   }
}
void loop()
{
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, LOW);    // set I/O pins as “low”, turn off LEDs one by one.
     delay(200);        // delay
   }
   for (int i = BASE; i < BASE + NUM; i ++) 
   {
     digitalWrite(i, HIGH);    // set I/O pins as “high”, turn on LEDs one by one
     delay(200);        // delay
   }  
}
```

### Output

> 

![]()

<!-- 
<HR>

## Experiment 

> 
  
### Components Required 

* 

### Circuit Diagram

![]()

### Code

```ino

```

### Output

> 

![]()
 -->
