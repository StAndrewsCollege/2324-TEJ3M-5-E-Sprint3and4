# 2324-TEJ3M-5-E-1-Sprint2
Second sprint for RoboCup line rescue Competition

Teammates: Richard Zhao, Shuiyi Zhao, Hendry Shao

## Process

The steps outlined below are for my RoboCup robot progress for 2 weeks (February 13th - February 28th)

### Goal Setting

The current robot has 4 motors and 2 TCS3200 sensors below the chassis. The code, however, only runs 2 motors and the motors typically have enough power to get up the ramps in the line following course, with some instances of the motors not being powerful enough. 
2 of the motors are at the same position as the TCS3200 sensors, which are at the front, while the robot is rear-wheel drive. The 2 TCS3200 sensors and the 2 front motors that aren't being used are in the same position, so I need to create a solution that allows for the TCS3200 sensors to be added in the same position without hurting the robot's movement up ramps. If I just put the sensors below the motors, the robot has a terrible ability to move and go up ramps as it comes in the way of movement in the front, and it has a similar issue when going down ramps. 
The solution needs to solve the issue of the sensors and motors being in place and allow for the robot to go up the ramps at a better rate (always has the power to go up the ramp)

The current robot has motor placement as seen in the photo
![20240222_164318](https://github.com/StAndrewsCollege/2324-tej3m-5-e-2-sprint2-Pranay-Ranjan/assets/118148551/4be0e7d9-37ad-4e43-995b-fa3677226035)

The TCS3200 sensors are planned to go right in the place of the motor on the right side of the photo

### Research

Teammates: Richard Zhao
- Richard gave the current code of the robot with my additions that run the rear-wheel drive

Personal knowledge:
- I have knowledge of how the motors work and how the rear-wheel drive currently operates
- I understand how the "tank" wheels operate
- Some sort of rearrangement of hardware will be required

Other Group in RoboCup - Harrison Chen's group: 
- They had a small axle-like piece of metal for each wheel that allowed for different speeds in turning
- This idea seems viable to remove the motors while keeping the tank wheels

Another group in RoboCup:
- This group had 4 motors and their colour sensors in front of the 4 motors while still being able to go up the ramp
- They only had similar TCS3200 colour sensors and no other colour sensors
- They recommended a change in idea to have the code of the TCS3200 colour sensors run both green square detection and line following

Web Resources:
- [OSEPP](https://www.osepp.com/electronic-modules/sensor-modules/58-color-sensor-module) (TCS3200 Data sheet from Google) (Colour sensor info sheet)
- [RoboCup Rules](efaidnbmnnnibpcajpcglclefindmkaj/https://junior.robocup.org/wp-content/uploads/2023/10/RCJRescueLine2024RulesDraft.pdf) (Rulebook, used to check for dimensional requirements)
- [Carnegie Mellon University](//efaidnbmnnnibpcajpcglclefindmkaj/http://cmra.rec.ri.cmu.edu/products/revol1_teachers/lesson/anytime/ramp/Notes.pdf) (What it takes for a robot to be controlled moving down ramps, helped in contextualizing problems)
- [RoboCup-made Forum](https://junior.forum.robocup.org/t/tutorial-for-building-and-programming-a-robot-for-rescue/792/2) (Placement of motors and sensors discussions)
- [Robotics Stack Exchange](https://robotics.stackexchange.com/questions/2491/how-are-color-sensors-used-for-line-following) (Placement of motors and sensors discussions)
- 
### Ideation

Based on research from people doing similar things and from teammates, I made 2 main ideas for how to remove the motors while keeping the wheels intact

#### Idea 1: Small Axles **(chosen to be prototyped)**
- Create small axles for the front 2 wheels
- Use 3-5cm axle pieces found in the makerspace
- Use bolts, spacers, etc. to make a wheel system that keeps the wheel in place
- Solves the weight issue by getting rid of 2 motors
- Might have some mild issues with going up ramps as now where there is, on occasion, a power issue

Image of the axle piece connected to a wheel - found in the makerspace

![IMG_6916](https://github.com/StAndrewsCollege/2324-tej3m-5-e-2-sprint2-Pranay-Ranjan/assets/118148551/0a33b555-570e-4f30-8a53-87704a89e717)

#### Idea 2: Screws to keep Wheels on
- Use the red metal pieces and connect them to the base
- Set red pieces vertically
- Use a screw to connect the wheels to the red piece
- Screws likely won't be a viable option for wheels
- Grooves might hinder the wheel performance
- Might solve weight issue but might not have enough motor power

Sketch of what the idea could look like: 

![Sketch](https://github.com/StAndrewsCollege/2324-tej3m-5-e-2-sprint2-Pranay-Ranjan/assets/118148551/8b2e560f-fa76-4d30-965c-ba923b061bc2)


#### Idea 3: Remove the line following sensors & only use the TCS3200 colour sensor for everything
- Keep 4 motors on the robot
- Remove the rectangular colour sensor from the front
- Code the TCS3200 colour sensor to correct when seeing black lines
- Likely won't resolve the ramp issue
- Likely still won't be a lot of space in front for the TCS3200 colour sensors

Sketch of the transition:

![Sketch2](https://github.com/StAndrewsCollege/2324-tej3m-5-e-2-sprint2-Pranay-Ranjan/assets/118148551/5e38b4a2-c88c-4a7a-909b-b955929082e5)

### Prototyping
Using the small axle design (Idea 1) with a small axle, 2 bearings, a small screw and a metal nut, I made a prototype of how the wheels could work. This prototype can be tested by seeing if the wheels move, if the tank wheels fit, etc. 

![20240222_164311](https://github.com/StAndrewsCollege/2324-tej3m-5-e-2-sprint2-Pranay-Ranjan/assets/118148551/566d1061-6a62-4177-99d1-5a2d889b6731)

This was done on one side of the robot to make this test as quick as possible (it took 20 minutes)
A couple of Allen keys and screwdrivers were used, but no overly complicated machines
This prototype made it so that the motor on one side was completely replaced with the axle which was able to show a proof of concept and prove that the idea in general works. 

This design made the wheels move smoothly, but there were many issues that might lead to a new direction or new design in total. 


### Testing and Critique

Good things about the prototype: 
- Wheels move very smoothly
- Motors are taken out from the front wheels
- Works as a solution to fit colour sensors
- Bearings fit well

Challenges:
- The wheel wasn't at the same height as the rear wheels which have the motors (Idea issue, didn't think about this issue)
- The wheels weren't on the same plane (weren't in line) (Prototype issue, wasn't able to add more parts)
- The tank wheel covering didn't fit as a result of the 2 challenges (Prototype issue)

Possible improvements: 
- Put in place a spacer to make the wheel on the same plane as the rear wheels
- Insert a piece of metal that makes the axle lower than it currently is

Next Steps - what will change/be added: 
- Prototype how to put a spacer with the current axle (the spacer doesn't fit on the axle piece)
- Find a way to add a rectangular red piece of metal (body pieces) to make the wheel lower
- Some ideation will need to be done for both of these changes/additions

Sketch of possible fix: 

![Sketch3](https://github.com/StAndrewsCollege/2324-tej3m-5-e-2-sprint2-Pranay-Ranjan/assets/118148551/162a92a7-b854-43f9-87d6-c411ce11f7e5)

### Final design

The final design of the robot's new wheel system is as follows

Materials to change the design: 
- 2 axle-like pieces
- 2 bolts that fit the axle pieces
- 2 spacer pieces
- 2 rectangular red metal pieces (body parts) cut to fit only the area of the wheel - 3x3
- 4 bearings (2 pairs)
- As many screws and corresponding bolts as needed


Steps to change the build to the final design: 
- Unplug the 2 front motors from the Arduino Mega 2560
- Unscrew the screws and washers on the red circular piece connected to the motor
- Take off the motor
- Using some screws, bolts, and red metal pieces, screw in the red piece on the current base on the lower rail
- Take the wheel that was connected to the motor and insert a pair of bearings with hands
- Insert the axle on the outside, with the grooved side on the inside with hands
- Put a bolt on the inside to keep the axle in place using a screwdriver on the screw side and holding together using a hand
- Put the wheel on the outside
- Insert and tighten a screw at the outside end of the axle to keep the wheel in place using the appropriate Allen key
- Repeat for the other side!

What one side looks like: 

![20240222_164315](https://github.com/StAndrewsCollege/2324-tej3m-5-e-2-sprint2-Pranay-Ranjan/assets/118148551/caf457fc-cdd2-4bd7-9e3b-729b295bfdff)

I couldn't get more photos of the robot's final design because I ran out of time at the end of class and RoboCup sessions, but the final design was refined to the point that the additions made it as though the wheels were the same as before, just motorless. This sprint was mainly hardware-focused with some usage of electronics in the placement and optimal usage, but it was majorly hardware-oriented. 


After implementing the final design that I explored above, I realized that there was an inherent issue with the current design of the robot's base and motors that needed to be addressed - it was too heavy. I was able to make a working model that I attempted to build and it worked well. The robot was able to turn well and move on the flat surface very well. The motor replacement was needed and it worked well with the TCS3200 colour sensors replacing them, but then the ramp came into play. When I tested the robot to see if the weight issue was fixed and the robot could go up the ramp every time, the robot failed. The robot could not make it up the ramp even 50% of the time, which cannot be used in a competition. 

This makes me think that the "final design" that I made isn't a final but rather a temporary solution. I, along with my group, will need to figure out a way to either add the motors back onto the robot, change the base design, remove the line following sensor, or find a way to reduce the weight of the robot. One of these solutions could actually be a "final design" as this would actually solve the problem. 

In total, this final design works in finding a way to put the TCS3200 colour sensor in place and making a way for the wheels to work if the motors were in fact removed, but there is an issue in this design that needs to be fixed. 

### Conclusion

This Sprint resulted in successes and knowledge of the need for future work. The successes were that I found a way to put the colour sensors that we have in the right place and make the front wheels work without the need for motors. I was also able to lower the weight of the robot by ~500 grams, which helped in the robot's overall movement. After creating the final design, and taking feedback from my prototype, I found that there were problems that needed to be addressed when testing the robot on the RoboCup course. The robot simply could not get up the ramp more than 50% of the time, which is a big problem. This problem will need to be addressed in the future, but the overall concept design works. 
