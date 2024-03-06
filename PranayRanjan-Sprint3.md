# 2324-TEJ3M-5-E-1-Sprint3
Second sprint for RoboCup line rescue Competition

Teammates: Richard Zhao, Shuiyi Zhao, Hendry Shao

## Process

The steps outlined below are for my RoboCup robot progress for multiple weeks (February 29th - April 4th)

### Goal Setting

In the RoboCup competition, there is a section of the line following course called the "rescue" section. In this section, we need the robot to navigate a line-less rectangle and collect balls to put them in their correct boxes inside the rectangular section. We don't have a way to pick up balls in this section and need something to do so to gain more points in the competition. 

The current robot doesn't have anything to pick up a ball or store the balls but we do have a way to find the balls in the first place. One of my teammates in RoboCup is trying to get a camera working in front of the robot to detect balls when they come into the camera's field of view. The robot will be able to navigate itself to the ball, but we don't have anything to pick it up. 

This sprint aims to find a way to pick up balls in this section of the competition. 

![](https://github.com/StAndrewsCollege/2324-TEJ3M-5-E-Sprint3and4/assets/118148551/2ebed059-bde1-4e0e-8611-2420038f2800)


### Research

#### Personal knowledge:
- Last year created a design for picking up balls
- Used a ramp-like system
- Pushed the ball against the wall
- Carried the ball in the curve
- Dropped the ball in the box backwards
- **Didn't work**

#### Other Group in RoboCup - Harrison Chen's group: 
- This group has made a claw/arm
- There is a claw at the end made of Lego pieces
- An arm is created from 3D printing
- Arm works from a Servo motor

#### Team BitFlip in RoboCup German National 2023
- https://youtu.be/3Ero-oU5lw4
- In this team's design, they made an arm, claw, and a box in the back to hold the balls
- Using a camera or ultrasonic sensor, they detect balls
- Went close to the ball, then put the arm down and close the claw
- The arm goes back all the way and drops the ball in its box
- The robot locates the box and opens its box's gate to drop the ball in

#### Brazil Team in RoboCup International 2023
- https://www.youtube.com/watch?v=Ly3G3CRP-Ls
- They were not able to pick up any balls, but the design is interesting
- They had a servo motor for the up/down motion of their collecting system
- There were 2 vertical sides to the collector and they converged while going down to become horizontal and pick up the ball
- They then held the ball in its collector and dumped the ball in the sorting boxes when done

#### Web Resources:
- [RoboCup Rules](efaidnbmnnnibpcajpcglclefindmkaj/https://junior.robocup.org/wp-content/uploads/2023/10/RCJRescueLine2024RulesDraft.pdf) (Rulebook, used to check for dimensional requirements)
- https://docs.rs-online.com/0e85/0900766b8123f8d7.pdf
- https://www.parallax.com/product/parallax-standard-servo/
- https://forum.arduino.cc/t/controlling-the-parallax-standard-servo/129007


### Ideation

Based on research from forums, videos, and other RoboCup groups regarding the ball-picking system, I created 3 possible ideas to combat the issue at hand

#### Idea 1:  Servo connected to Arm & Shuiyi Invention **(chosen to be prototyped)**
- In Shuiyi Zhao's last Sprint he created a mechanism to pick up balls
- He made an upside-down cup shape with rubber bands to hold the balls while allowing them to go through
- He has also created an arm of sorts from the same Sprint
- Connect the servo motor to the arm
- Have the servo motor turn up/down for the arm
- The ball gets picked up by Shuiyi's invention
- Arm lightly picks up the ball off the ground
- When approaching the sorting box, the arm extends all the way to drop the ball in the sorting box

#### Idea 2: Ramp With a Box in the Back
- Build a ramp from metal and Lego
- Connect the servo motor to the ramp to move up/down
- Hold balls in the front but above ground
- There isn't a clear way to put the balls in the correct boxes
- It didn't work last time
- Need to go to walls, ball can roll away in the process

#### Idea 3: Claw in the Front & Box in the Back
- Use a gear to make a claw open/close
- Connect the servo motor to the arm
- Calculate how far the ball should be for the claw to pick up
- Put arm down to ball level
- Gear moves and the ball gets collected by claw
- Put the arm up and open the gear to drop the ball in a box behind the arm
- Box opens when the sorting boxes are near
- Claws can be innacurate
- The ball sometimes slips out of the claw depending on materials
- Gear is very complicated to create
- Need 2 motors for this idea


### Prototyping



### Testing and Critique

#### Good things about the prototype: 
- 

#### Challenges:
- 

#### Possible improvements: 
- 

#### Next Steps - what will change/be added: 
- 

### Final design

The final design of the robot's 

#### Materials to change the design: 
-


#### Steps to change the build to the final design: 
- 


### Conclusion


