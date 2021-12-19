# Experiment 8 - Flame Sensor

> An experiment to understand the working of an Flame sensor.

### LDR : Light Dependent Sensor

> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.

![image](https://user-images.githubusercontent.com/51323070/146687534-a4c7ee74-cd88-4af2-96b8-581b63758aee.png)

### Components Required

* Arduino Uno Board*1
* Flame Sensor *1
* Buzzer *1
* 10K Resistor *1
* Breadboard Jumper Wire*6
* USB cable*1

### Circuit Diagrams

![image](https://user-images.githubusercontent.com/51323070/146687216-bcb36fc2-20cb-44bd-9093-83e169b6512c.png)

![image](https://user-images.githubusercontent.com/51323070/146687218-0b4dcc4a-875e-4795-a968-9f3d55aa1b99.png)

### Code

```ino
int flame=0;// select analog pin 0 for the sensor
int Beep=9;// select digital pin 9 for the buzzer
int val=0;// initialize variable
 void setup() 
{
  pinMode(Beep,OUTPUT);// set LED pin as “output”
 pinMode(flame,INPUT);// set buzzer pin as “input”
 Serial.begin(9600);// set baud rate at “9600”
 } 
void loop() 
{ 
  val=analogRead(flame);// read the analog value of the sensor 
  Serial.println(val);// output and display the analog value
  if(val>=600)// when the analog value is larger than 600, the buzzer will buzz
  {  
   digitalWrite(Beep,HIGH); 
   }else 
   {  
     digitalWrite(Beep,LOW); 
    }
   delay(500); 
}
```

### Output

![loading](https://user-images.githubusercontent.com/51323070/146673156-df307713-2ec1-46dd-9e6f-5bd0c7afc81f.gif)
