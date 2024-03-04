# Problem
The robot can't follow a given path (line)

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
