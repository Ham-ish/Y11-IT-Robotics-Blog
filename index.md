# Y11 IT Robotics Blog 

## 7/11/22

Last week I rethought my idea for what a catupult does. Previously I had a preconception that the arm had to throw the payload "overarm", when I had the idea to go "underarm" instead. Creating a mechanism that hit a ball like a golf club into a ramp that launched it some variable distance was my new plan, and I immediately began working on prototypes.

I made the first prototype early in the week, which ment I could get it back and continue working on it early. The idea was to have a chanel that a ball would travel down, at which point it would be hit by the rotating arm and speed up greatly, then hitting the ramp and going into the air.


<img src="./Images/Golfpult prototype i.png" title="Golfpult prototype i" width="400"/>

<img src="./Images/Golfpult prototype i ball.png" title="Golfpult prototype i" width="150"/><img src="./Images/Golfpult prototype i hit.png" title="Golfpult prototype i" width="150"/><img src="./Images/Golfpult prototype i ramp.png" title="Golfpult prototype i" width="150"/>

So I 3D printed the pieces and found their main problems

1. It was very small
2. The swinging arm couldn't fit into the holders
3. There was no places for the mechatronic pieces to connect

So i fixed these problems and created this:

<img src="./Images/Golfpult prototype ii.png" title="Golfpult prototype ii" width="400"/>

I increased the scale of the model as well as increasing the size of the arm holders. I made points for the servo and motor to connect and also improved the model of the ramp

<img src="./Images/Golfpult new hole.png" title="Golfpult prototype ii" width="150"/><img src="./Images/Golfpult new fixing.png" title="Golfpult prototype ii" width="150"/><img src="./Images/Golfpult new ramp.png" title="Golfpult prototype ii" width="150"/>

I have not been able to test these pieces as they will take longer to print, and with the project deadline moving very close I am worried that it may not work the way it was supposed to.



Other than that the project still has some minor fiddlings to do, but overall I am still confident that the project is good. I have grown my understanding and skills in the areas of 3D printing and modeling, motors and servos, general coding and a new appreciation for the mechatronics subject and mindset.

## 31/10/22

Began working on catupult arm. 3D printed a stick with a ball holder on the end to attach to a servo, but the base was too poorly designed so has to use hobby motor instead. Attached them together with hot glue and then encountered a problem. The motor doesn't have enough torque to rotate the arm with a weight on it.

<img src="./Images/High speed paper cutter (gear).JPG" title="High speed paper cutter (gear)" width="500"/>

The contraption was, however, capable of rotating at a decent speed and build up some angular momentum and so, in an effort to make the time spent in 3D printing and building not go to waste, it was decided that this device would become a saw. So the scooped head was removed and the edge was sharpenedin an attempt to reduce surface area and therefore make a better cutting edge, but cutting against th layered "grain" of 3D printed materials is not very effecitve, so shaped hot glue was used instead. 

<img src="./Images/High speed paper cutter (paper).JPG" title="High speed paper cutter (paper)" width="500"/>

This is a prime example of a mechatronic device, using electricity, motors and simple machines to achieve somthing new and exciting.

<img src="./Images/High speed paper cutter.JPG" title="High speed paper cutter (battery)" width="500"/>

On a more useful note, I have changed the code for the ultrasonic servo so that it now has a range of more than 50 cm

<img src="./Images/Ultrasonic test 2.png" title="Ultrasonic servo Code" width="300"/>

Servo was twitching because it occasionally read 0 from the ultrasonic, so I changed the delay and now it doesn't do that until the sound-bounced object is more than 50 cm away. I also mapped the ultrasonic values between 0 and 56 cm to angles on the servo, so now it moves 180 degrees between maximum and minimum values. Turns out the Servo.h library is pretty funky. 

The tissue cutting caupult taught me about the type of torque that the catupult might have, and inspired a possible solution in my final build.



## 24/10/22

Created code to move a servo to aim the catupult 

<img src="./Images/Ultrasonic Test 1.png" title="Ultrasonic servo Code" width="300"/>

<img src="./Images/Ultrasonic servo test 1.jpg" title="Ultrasonic servo build" width="300"/>

The code uses the ultrasonic to send a pulse and receive a pulse and then using the speed of sound as a constant to measure the distance. It then changes the angle of the servo based on the distance. It currently twitches wildly if the ultrasonic senses anything further away than 10 cm.

## 17/10/22

Blog post about last weel of Term 3 and week 1 Term 4

**Term 3 end**

Learning whether a PIR sensor does the things that I think that it does, realising that it is not nearly as directional as I thought it was and trying to find a solution before I forget about it.

**Term 4 week 1**

having completely forgotten about the previous problem, I started using pirs in TinkerCad and created a simple circuit.

<img src="./Images/Tinkercad PIR test 1.png" title="Array Led Code" width="300"/>

Which I then realised was the exact same as the tutorial PIR LED circuit.

<img src="./Images/Tinkercad PIR tutorial 1.png" title="Array Led Code" width="175"/>

It is now my idea to use ultrasonics to measure distance then angle and tention the catapult based on the distance within a range of a few meters

## 19/9/22

Practical project preface issued, I need to make a cool robot again

This time, the robot needs to do thoings

**Planning and Preperation**

Build a robot that takes movment sensor data to aim and fire a projectile

We have Motion sensors 

I am going to learn how they work to see how plausable this idea is

Otherwise

Building an aiming system for a 3D printed catupult will be what i am doing

I am still in the exploration stage of this assignment and have no idea what i will actually do

## 12/9/22

EEPROM

Storing information inbetween lack of power

EEPROM makes it possible to store non-volitile data. 

This is the code that the build uses.

<img src="./Images/EEPROM Code 1.png" title="EEPROM Code 1" width="600"/>

<img src="./Images/EEPROM Code 2.png" title="EEPROM Code 2" width="600"/>

This is the Board that the document provides

<img src="./Images/EEPROM Example Board.JPG" title="EEPROM Example Board" width="400"/>

The board should take the input from the button push and then use EEPROM to store the button state as non-volitile information and then print the output with serial.print and as an LED state, but the board schematic provided does not have an LED connected to pin 13, so it does not do that.

Conclusion

I couldn't test this board because I lost my USB-C Adapter 

## 5/9/22

Bit math

Using shift registries to read and compare 8 digit binary numbers, then show visually using LED's

<img src="./Images/Shift regestry code.png" title="Shift regestry code" width="300"/>

<img src="./Images/Shift regestry code 2.png" title="Array Led Code" width="300"/>

The code reads an decimal input from the user, converts it to binary, and compares that to a preset binary string using "And", "Or", and "Exclusive Or". This is then shown on the LED's, lighting up to show 1's and dimming to show 0's


<img src="./Images/Registerless hardware.jpg" title="Registerless hardware" width="300"/>

Here is the hardware

There is no shift register currently in the boxes so this is everything else in the hardware

Due to me changing my computer to windows, I have had to reinstall and reinitialise a lot of the things on the computer which has caused a few technical difficulties and delays


## 29/8/22

Exams

no work do

## 22/8/22

Exam week prep

no time for blog

sorry

## 15/8/22

This week of IT was mainly focused on game dev work and was therefore devoid of any substantial robotics


## 8/8/22

Finished Arduino Components document

Array Blinking Led

<img src="./Images/Array Led Board.JPG" title="Array Led Board" width="300"/>
<img src="./Images/Led pattern arrays.jpeg" title="Array Led Code" width="300"/>

Uses an array to reference which led to turn on in a line


## 1/8/22 

Worked on Arduino Components document

Completed Switch cases task

<img src="./Images/Switch cases test.png" title="Switch case tutorial" width="300"/><img src="./Images/Switch case Breadboard.JPG" title="Switch case breadboard" width="600"/>

This circuit uses a switch case to turn the many possible potentiometer values into a few cases to change the brightness of a led


<img src="./Images/Hypotenuse calculator code pt1.png" title="Hypotenuse calculator" width="800"/>

<img src="./Images/Hypotenuse calculator code pt 2.png" title="Hypotenuse calculator" width="800"/>

This code uses functions to calculate the hypotenuse of a triangle given opposite and adjacent sides

## 25/7/22 Begining of Term 3 Blog

Worked trough the PWM Document and created the circuits


<img src="./Images/Screen Shot 2022-07-24 at 9.29.40 pm.png" alt="Show screenshots" title="PWM_Tutorial_1" width="300"/>

<img src="./Images/PWM_Tutorial_2.png" title="PWM_Tutorial_2" width="300"/>

The images for the phisical build are being difficult so if they are not there it means that i couldnt fix it

-

-

-

-

-

-

##

## 2/5/22 Begining of Term 2 Blog

Simulated arduino circuitboard in tinkercad

<img src="Simulated_Circuit_code1.png" alt="Show screenshots" title="Mount Rushmore" width="300"/><img src="Simulated_circuit1.png" alt="Show screenshots" title="Mount Rushmore" width="600"/>


## 7/4/22 Turns out the Assignment was due

Turned in assignment 

Bionic ears can do stuff

Overveiw: Not great

## 28/3/22 Simple Arduino hardware Intro

Research Task issued

Requires to do research on a topic of robotics and mechatronics
-begun research on UNSW Bionic eye

Overveiw: not much happened

## 21/3/22 Simple Arduino hardware Intro

Missed Lesson on Monday Due to Public Holiday

Cyber Live

Begun cyber live course on grok

Screenshots

<img src="GrokCyberlive1_VampireHunters.png" alt="Show screenshots" title="Mount Rushmore" width="700"/>
<img src="GrokCyberlive2_SystemCompromised.png" alt="Show screenshots" title="Mount Rushmore" width="700"/>
<img src="GrokCyberlive3_DropByAndSayHi.png" alt="Show screenshots" title="Mount Rushmore" width="700"/>
<img src="GrokCyberlive4_AnotherPossibleTarget.png" alt="Show screenshots" title="Mount Rushmore" width="700"/>
<img src="GrokCyberlive5_TargetPractice.png" alt="Show screenshots" title="Mount Rushmore" width="700"/>


_____________________________________________

Arduino

Solved connection issue

Project 13

Fan Constantly spinning

Shouldn't do that

______________________________________________

Overview: Begun cyber live course work in class and therefore had less time to do Arduino work


## 15/3/22
Ardino project

Project 13

Encountered an error connecting the Controlling device to the arduino
Belived to be due to overdrawing power from device

______________

CyberSecurity preperation

CyberLive

Encrypting data in a file


Overveiw: Need to solve power problem for arduino and do GROK Cyber Course



## 7/3/22 Simple Arduino hardware Intro
Arduino projects 


**Projects from last week**

Project 3
Interactive Trafficlights

Arduino

<img src="ArduinoProject3.JPG" alt="Show screenshots" title="Mount Rushmore" width="300"/>

Code
 
<img src="ArduinoCode3.png" alt="Show screenshots" title="Mount Rushmore" width="300"/>



Project 4
Breathing LED


Arduino

<img src="ArduinoProject4.JPG" alt="Show screenshots" title="Mount Rushmore" width="300"/>

Code
 
<img src="ArduinoCode4.png" alt="Show screenshots" title="Mount Rushmore" width="300"/>




Project 5
Colour RGB LED


Arduino

<img src="ArduinoProject5.JPG" alt="Show screenshots" title="Mount Rushmore" width="300"/>

Code
 
<img src="ArduinoCode5.png" alt="Show screenshots" title="Mount Rushmore" width="300"/>





Project 6
Alarm


Arduino

<img src="ArduinoProject6.JPG" alt="Show screenshots" title="Mount Rushmore" width="300"/>

Code
 
<img src="ArduinoCode6.png" alt="Show screenshots" title="Mount Rushmore" width="300"/>




Project 7
Temperature Alarm


Arduino

<img src="ArduinoProject7.JPG" alt="Show screenshots" title="Mount Rushmore" width="300"/>

Code
 
<img src="ArduinoCode7.png" alt="Show screenshots" title="Mount Rushmore" width="300"/>




**Projects from this Week**

Project 8
Vibration Sensor


Arduino

<img src="ArduinoProject8.JPG" alt="Show screenshots" title="Mount Rushmore" width="300"/>

Code
 
<img src="ArduinoCode8.png" alt="Show screenshots" title="Mount Rushmore" width="300"/>




Project 9
Light sensitive LED


Arduino

<img src="ArduinoProject9.JPG" alt="Show screenshots" title="Mount Rushmore" width="300"/>

Code
 
<img src="ArduinoCode9.png" alt="Show screenshots" title="Mount Rushmore" width="300"/>





Project 10
How to Drive a Servo


Arduino

<img src="ArduinoProject10.JPG" alt="Show screenshots" title="Mount Rushmore" width="300"/>

Code
 
<img src="ArduinoCode10.png" alt="Show screenshots" title="Mount Rushmore" width="300"/>




Project 11
Controllable servo


Arduino

<img src="ArduinoProject11.JPG" alt="Show screenshots" title="Mount Rushmore" width="300"/>

Code
 
<img src="ArduinoCode11.png" alt="Show screenshots" title="Mount Rushmore" width="300"/>




Project 12
Interactive Adjustable RGB LED

Arduino


<img src="ArduinoProject12.JPG" alt="Show screenshots" title="Mount Rushmore" width="300"/>

Code
 
<img src="ArduinoCode12.png" alt="Show screenshots" title="Mount Rushmore" width="300"/>






Overveiw:

Continued use of new Arduino hardware, introducing pushbutton switchers, ambient light sensors, tilt switch sensors, busters, potentiometers and servos, and finding out how they interact with code






## 28/2/22 Robotics cont.


Arduino Projects

Project 3
Dynamic traffic lights

Code

ill do it next week
(technically not late)




## 21/2/22 Initial robotics


Micro:bits
Micropython

Show screenshots

<img src="Microbits_code1.png" alt="Show screenshots" title="Mount Fukushima" width="400"/>

<img src="Microbits_code2.png" alt="Show screenshots" title="Mount Rushmore" width="300"/>

<img src="Microbits_code3.png" alt="Show screenshots" title="Mont Blanc" width="300"/>

<img src="Microbits_code4.png" alt="Show screenshots" title="Mount Cilindro de Marboré" width="350"/>

Arduino projects 

Project 2
LED SOS Signal

Arduino

N/A

Code
 
 ![Show screenshots](./Codescreenshot1.png "San Juan Mountains")

Project 3
Dynamic traffic lights

Arduino

N/A

Code

N/A

Overveiw:

Beginning a new topic with basic breadboards and c++
