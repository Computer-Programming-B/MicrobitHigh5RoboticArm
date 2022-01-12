# Build a "High 5" Robotic Arm
In this project, you will be using the micro:bit and a type of motor called a *servo* to move a robotic arm. The micro:bit light sensor will trigger the servo, so that when a shadow of a hand passes over the LED array, the arm rotates into a "high 5" position.

### Step 1: Connect the servo to the micro:bit
Our Robotic Arm project will use the following parts:
- micro:bit
- Servo
- Alligator cables to connect the micro:bit to the servo
- Robotic arm (popsicle stick with hand cutout and servo mount) 

Use the following circuit diagram to connect the servo to the micro:bit with the alligator cables.   
![](MicrobitServoConnections.png)   

### Step 2: Run this sample program

```python
from microbit import * 
# Servo control: 
# 50 = ~1 millisecond pulse all right 
# 75 = ~1.5 millisecond pulse center 
# 100 = ~2.0 millisecond pulse all left 
left = Image("00900:09300:99999:09300:00900")
right = Image("00900:00390:99999:00390:00900")
stop = Image("00900:09390:93039:09390:00900")
pin0.set_analog_period(20)

while True: 
	pin0.write_analog(50) #turn clockwise
	display.show(right)
	sleep(1000)
	pin0.write_analog(75) #stop turning
	display.show(stop)
	sleep(1000)
	pin0.write_analog(100)
	display.show(left) #turn counterclockwise
 	sleep(1000)
 	pin0.write_analog(75) #stop turning
	display.show(stop)
	sleep(1000)
```
You should see the servo spin clockwise for 1 second, stop spinning for 1 second, spin counterclockwise for 1 second, stop spinning for 1 second and then repeat like the video below:   
![](ServoTest.gif)   

### Step 3: Build the Robotic Arm and attach it to the servo
There may already be a popsicle stick arm in your kit. If not, you will need to make one. Ask your teacher for a print out of a hand and a glue gun. Cut out the hand and glue it to one end of the stick. Glue the servo mount from your kit to the **side** of the popsicle stick at the other end.     
![](Hi5-1.png)   
Attach the robotic arm to the servo by pressing it into place.   
![](Hi5-2.png)   

### Step 4: Write the program
TBD

### Step 5: Submit your finished program
Submit your Python code and an animated gif of your program running
