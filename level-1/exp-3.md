# Experiment 3 - LED Chasing Effect

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
int BASE = 2 ;  // the I/O pin for the first LED
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

![loading](https://user-images.githubusercontent.com/51323070/146673156-df307713-2ec1-46dd-9e6f-5bd0c7afc81f.gif)