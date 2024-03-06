# Problem
The robot can't follow a given path (line). I need the robot to constantly look for and follow a black line. 

The bot once did, but after some huge adjustments, it doesn't work again. Have to start over. 

# Ideation & Research

Potential sensors to install
- Line follower/IR sensor
- Color sensor
- Image sensor
- Photoresistor

Line follower/IR sensor
https://www.infratec.eu/sensor-division/service-support/glossary/infrared-sensor/

- Operates a simple mechanism, based on the reflection of IR rays; Inaccurate for color, but good for differentiating
- Available line follower has multiple IR sensors installed together; Will save wiring space by A LOT

Color sensor
(Based on Sprint2's experience)

- Too many wires, color sensors for turns, and considering a potential extra color sensor, too many wires
- Will need to install multiple as the detection range is very limited

Image sensors
https://www.instructables.com/OV7670-Arduino-Camera-Sensor-Module-Framecapture-T/

- Unnecessarily complicated for a simple black line to white surface differentiation
- Too many wires, color sensor wiring already took up too much

Photoresistor
https://blog.arduino.cc/2017/08/30/rgb-led-color-detector/

- Single target based, need to install multiple to compare 2 surfaces simultaneously

### Solution
IR sensor/Line follower

# Research
http://wiki.sunfounder.cc/index.php?title=Line_Follower_Module

Provides general info about the Sunfounder line follower module
- Each black bit is an IR sensor, where one side shoots an IR ray and the other detects the intensity of the ray
- Provides wiring info; 5V - 5V pin, GND - GND pin, SCL - A5 pin, SDA - A4 pin
- Provides code that makes the sensor work

``` C++
#include <Wire.h>
#define uchar unsigned char
uchar t;
//void send_data(short a1,short b1,short c1,short d1,short e1,short f1);
uchar data[16];
void setup()
{
  Wire.begin();        // join i2c bus (address optional for master)
  Serial.begin(9600);  // start serial for output
  t = 0;
}
void loop()
{
  Wire.requestFrom(9, 16);    // request 16 bytes from slave device #9
  while (Wire.available())   // slave may send less than requested
  {
    data[t] = Wire.read(); // receive a byte as character
    if (t < 15)
      t++;
    else
      t = 0;
  }
  Serial.print("data[0]:");
  Serial.println(data[0]);
  Serial.print("data[2]:");
  Serial.println(data[2]);
  Serial.print("data[4]:");
  Serial.println(data[4]);
  Serial.print("data[6]:");
  Serial.println(data[6]);
  Serial.print("data[8]:");
  Serial.println(data[8]);
  Serial.print("data[10]:");
  Serial.println(data[10]);
  Serial.print("data[12]:");
  Serial.println(data[12]);
  Serial.print("data[14]:");
  Serial.println(data[14]);
  delay(500);
}
```

https://www.arduino.cc/reference/en/language/functions/communication/wire/

Further explains the code above - What's the Wire.h library?

- Wire.h allows the code to communicate with I2C devices
