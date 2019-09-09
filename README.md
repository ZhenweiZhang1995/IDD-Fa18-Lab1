# IDD-Fa18-Lab1: Blink!

**A lab report by John Q. Student**

**Fork** this repository to get a template for Lab 1 for *Developing and Designing Interactive Devices* at Cornell Tech, Fall 2018. You should modify this `README.md` file to delete this paragraph and update below. As the lab asks:

> Include your responses to the bold questions on your own fork of the lab activities. Include snippets of code that explain what you did. Deliverables are due next Tuesday. Post your lab reports as `README.md` pages on your GitHub, and post a link to that on your main class hub page.

We've copied the questions from the lab here. Answer them below!

## Part A. Set Up a Breadboard

![Image1](https://github.com/ZhenweiZhang1995/IDD-Fa18-Lab1/blob/master/image1.jpg)


## Part B. Manually Blink a LED

**a. What color stripes are on a 100 Ohm resistor?**   
Brown, Black, Brown, Gold
(Band, Band, Multiplier, Tolerance)
 
**b. What do you have to do to light your LED?**  
Connect the circuit as the diagram, connect the metro mini to the computer using the USB cable, and then press the switch.


## Part C. Blink a LED using Arduino

### 1. Blink the on-board LED

**a. What line(s) of code do you need to change to make the LED blink (like, at all)?**  
Nothing needs to be changed from the “Blink” example code

**b. What line(s) of code do you need to change to change the rate of blinking?**  
Change the parameter in delay()

**c. What circuit element would you want to add to protect the board and external LED?**  
A resistor.
 
**d. At what delay can you no longer *perceive* the LED blinking? How can you prove to yourself that it is, in fact, still blinking?**  
 I can no longer perceive the LED blinking at delay(10) which is 10ms. I can prove it is still blinking by look at it through the camera on my phone. The LED will be blinking on my phone because the camera have a slower refresh rate.

**e. Modify the code to make your LED blink your way. Save your new blink code to your lab 1 repository, with a link on the README.md.** 
[Modified_blink](https://github.com/ZhenweiZhang1995/IDD-Fa18-Lab1/blob/master/Blink_modified.ino)


### 2. Blink your LED

**Make a video of your LED blinking, and add it to your lab submission.** 

[Video here](https://youtu.be/6gIY8t9rgQg)


## Part D. Manually fade an LED

**a. Are you able to get the LED to glow the whole turning range of the potentiometer? Why or why not?**  
The LED is able to glow the whole turning range of the potentiometer.This is becuase total voltage is set, and from Ohm's Law, we know the larger resitor will have higher voltage, thus the voltage of the LED will be smaller.

## Part E. Fade an LED using Arduino

**a. What do you have to modify to make the code control the circuit you've built on your breadboard?**  
On Line 18, change the PIM from 9 to 11
`led = 9`  to `led = 11`

**b. What is analogWrite()? How is that different than digitalWrite()?**  
The digitalWrite() method sets the value of a digital pin as HIGH or LOW.  
The analogWrite() method sets the value of a PWM output pin. The analogWrite() is on a scale of 0 - 255, such that analogWrite(255) requests a 100% duty cycle (always on), and analogWrite(127) is a 50% duty cycle (on half the time).


## Part F. FRANKENLIGHT!!!

### 1. Take apart your electronic device, and draw a schematic of what is inside. 

**a. Is there computation in your device? Where is it? What do you think is happening inside the "computer?"**  
Yes, it is on the micro-controller board. It accepts signal from the button and display content on the screen/play radio through the speaker

**b. Are there sensors on your device? How do they work? How is the sensed information conveyed to other portions of the device?**  
Yes, there is pressure sensor on the clock radio. The sensed information is conveyed through jump wire connected between sensor and micro-controller.

**c. How is the device powered? Is there any transformation or regulation of the power? How is that done? What voltages are used throughout the system?**  
The radio is powered with 120V power outlet. It transforms the voltage from 120v to 5v. This is done through the power adaptor for the radio. 5V voltage is used throughout the system.

**d. Is information stored in your device? Where? How?**  
Preset radio channels are stored in the radio. This information is stored inside the micro-controller.

### 2. Using your schematic, figure out where a good point would be to hijack your device and implant an LED.

**Describe what you did here.**

### 3. Build your light!

**Make a video showing off your Frankenlight.**  
[My Frankenlight on the radio](https://youtu.be/modgPDKQcg8)

**Include any schematics or photos in your lab write-up.**
