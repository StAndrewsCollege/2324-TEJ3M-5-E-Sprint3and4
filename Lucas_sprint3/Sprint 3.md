[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/mlnznQ98)
# 2324-TEJ3M-5-E-1-Sprint1
Our first evaluative sprint for the roboCup project. Within this sprint you will be identifying and developing a specific personal goal to achieve within your team's development of your competition robot. For this sprint you will be defining your own goals, researching, designing, prototyping, testing, refining and documenting your process.

You will submit this work by committing changes to this repository. Add all information, links, images, code, design files to this repository.


> [!IMPORTANT]
> This sprint will take 5 classes, being submitted on Monday February 12th

If you have not developed a robot before, or are starting from scratch, the following initial goals are suggested
- Learning about motor controllers and getting wheels turning
- Learning about distance, colour or line following sensors, and writing code to make decisions based on measured values
- Designing and building a simple chassis for your robot to hold the microcontroller, motors, sensors

## Process

You will follow the steps outlined below (for both this sprint and those for our RoboCup design).

### Goal Setting

The robot will move through the maze and look for victims, based on the colour and shape of the 'victims', they will recieve different amounts of supplies. A H shaped victim recieves 2 packages, a U shaped vicitm recieves 1 package, and an S shaped vicitm recieves no packages. Red vicitms receive 2 packages, yellow victims will receive 1 package, and green victims get no packs. By using a camera, and a detection system (either pixel comparison, literally just AI, or haar cascade), we can differentiate between the victims. Therefore, my goal is to make a camera and camera program which can differentiate between victim's shapes and colours.

### Research

The camera we are using is the OpenMV H7 Plus (Product page: https://openmv.io/products/openmv-cam-h7-plus). The first step is to simply get an image in the first place.
https://docs.openmv.io/openmvcam/tutorial/index.html <- contains some code which be useful?

Haar cascade informtaion + code in C++, Java, and Python (how convenient):
https://docs.opencv.org/3.4/db/d28/tutorial_cascade_classifier.html

Pixel comparison information:
https://support.smartbear.com/testcomplete/docs/testing-with/checkpoints/regions/how-image-comparison-works.html

There is less information on pixel comparison, and search results are clouded by other topics with similar names, but which do not contain information relevant to the robot. However it is simple enough to understand. Snapshot to snapshot, the robot compares the image with a previous image. Depending on how the pixels within the image line up, it will be able to identify shapes. For example, if the comparion image is a known letter "H", and the pixels which match up from the snapshot taken from the camera match up to the "H", then we will know that the robot is facing an H victim, and will deposit 2 supplies.

It is most likely that AI will be used over pixel comparison or the haar cascade. More reseach will need to be done, but my team members say that this is what they used the year prior, and that there is already semi-functional code, as well as a way to easily create new code/AIs.

https://www.tensorflow.org/learn: Will be used to figure out the AI.

### Ideation

There should be no issues with using AI for the algorthim for the robot. Despite the fact that I'm not fully sure how it works yet, I have been told that the setup for the AI is very simple. Thus, we will probably be using AI, as it has both been figured out by the team last year (at least so some degrees）and also because it is the most advanced/accurate compared to pixel comparison or a haar cascade. There's really no ideation for the camera. So long as I can get it running (that is to say that the camera can generate and image and return it back to the robot it should be fine (also that is it wired correctly, but that of course is included in the "collecting and returning image" part). For now, I'm unsure about the method with which I will make the AI, however, it has been determined that that is the image detection system we are going to use. In terms of the camera code, it operates in python for some reason, so I'll have to speedrun the learning on that if I am to finish the setup and the algorithim by the end of this sprint. The sensors are fully dealt with, all that's left is to await a replacement for the single broken one, wire them together, make sure they're working (running on old code from last year) and that's it.

The code for the colour detection is pretty much built into the camera itself. All we have to do is write the code, we don't need to train and use an AI to detect colour. For the shape detection, we will be using an AI built using TensorFlow (what the team used last year). It will be trained to detect Hs, Us, and Ss. If nothing goes wrong, the maze should only contain these items, with nothing that may be confused for a victim.

### Prototyping

You will make a quick and simple test of your ideas, making something that is built and tested as quickly as possible.

### Testing and Critique

You will evaluate your prototype and document your thinking, what you have learned and how you will improve your design.

### Final design

You will document your final design idea in detail, with enough technical detail for another engineer to recreate your work

### Conclusion

You will make a brief comment on the success of your design and what next steps others might build on your work.

## Evaluation
For each sprint that we undertake in class, we will work to produce and be assessed on the same following steps. The Success Criteria below will form your assessment, each being measured on levels 1-4.

Level 1 - serious errors or misunderstandings of expectations

Level 2 - some errors or areas where expectations are not met

Level 3 - all course expectations are fulfilled

Level 4 - work exceeds course expectations, or specific areas of quality can be identified

### Success Criteria

#### Goal Setting 

- Goals identified are clearly described and testable (will we know if you succeed? how?) 
- Goals identified are within the scope (can they be completed in ~2 weeks, do we have the materials, equipment and expertise to complete these?) 
- Goals make meaningful progress towards final robot design (this is a goal that will help your team) 

#### Research

- Research has been used to investigate the goal and possible solutions (you've used research to help you)
- Research has been sourced from reputable, technical sources (we can trust where you got your information)
- What information came from where is clearly indicated (another person knows what information is yours, what came from elsewhere, and where it came from. Another person could continue your work by learning from these sources, or check your information.)

#### Ideation

- Initial planning and thinking is shown for each step/decision (thinking is outlined with notes, sketches, code snippets, or whatever method is fastest to record this thinking)
- Initial planning and thinking shows a breadth of ideas (several ideas have been considered and documented, it is clear why one idea is being favoured over another.)

#### Prototyping

- Prototype is created to test a specific idea that is outlined in ideation (what is being tested and how it will be tested is clear)
- Prototype is rough and quick, only as refined as it needs to be to test the idea (it is clear care has been taken to choose the fastest way to test the idea)

#### Testing and Critique

- Prototype is documented along with clear explanation of what has been learned (Did it work? what will be improved for next steps? What problems need to be fixed in the design itself, and what are inherent to the roughness of the prototype?)
- Next steps are clearly outlined to improve the design (what will change about the next design, may include new research/ideation).

#### Final design (for the sprint)

- Design shows direct inspiration and improvement from ideation/prototyping stages (it is clear how you got to this design)
- Design is refined and polished given the scope of the sprint (care, resources and talent have been used to make this design as complete as possible given the time and constraints)
- Design has used technical skills learned in class to create the final product (learning of electronics, code, 3D or 2D design evident).
- Design shows specific skill in the use of tools, and the selection of appropriate tools (skill in tool use is evident, and if simpler tools could achieve the same result they have been used instead).

#### Conclusion

- A brief statement clearly outlines the specific successes or future work needed for the design. Audience is another student engineer who may want to build on this work. (Specific, detailed but concise, useful as an overview for other students who want to learn from your sprint.)
