# Experiment 7 - LDR Light Sensor

> An experiment to understand the working of an LDR light Sensor.

### LDR : Light Dependent Sensor

> Photo Resistor (Photovaristor) is a resistor whose resistance varies from different incident light strength. It's based on the photoelectric effect of semiconductor. If the incident light is intense, its resistance reduces; if the incident light is weak, the resistance increases.

![L5Iw9_3102_1628755894](https://user-images.githubusercontent.com/91405741/138436746-d1cfb008-0d90-4754-b4c4-fe133329c8b5.png)

### Components Required

* Arduino Uno Board
* Photo Resistor*1
* Red M5 LED*1
* 10KΩ Resistor*1
* 220Ω Resistor*1
* Breadboard*1
* Breadboard Jumper Wire*7
* USB cable*1

### Circuit Diagrams

![image](https://user-images.githubusercontent.com/51323070/146687216-bcb36fc2-20cb-44bd-9093-83e169b6512c.png)

![image](https://user-images.githubusercontent.com/51323070/146687218-0b4dcc4a-875e-4795-a968-9f3d55aa1b99.png)

### Code

```ino
const int ledPin = 13;
const int ldrPin = A0;
void setup() {
    Serial.begin(9600);
    pinMode(ledPin, OUTPUT);
    pinMode(ldrPin, INPUT);
}
void loop() {
    int ldrStatus = analogRead(ldrPin);
    if (ldrStatus <= 200) {
    digitalWrite(ledPin, HIGH);
    Serial.print("Its DARK, Turn on the LED : ");
    Serial.println(ldrStatus);
} 
else {
    digitalWrite(ledPin, LOW);
    Serial.print("Its BRIGHT, Turn off the LED : ");
    Serial.println(ldrStatus);
}
}
```

### Output

![loading](https://user-images.githubusercontent.com/51323070/146673156-df307713-2ec1-46dd-9e6f-5bd0c7afc81f.gif)
