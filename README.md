# Servo Motor Interfacing 

##  AIM:
To control the speed and direction of servomotor using Arduino UNO controller.

## Software required:
Arduino IDE </br>
Proteous

## PROCEDURE:
### Arduino IDE
Step1:Open the Arduino IDE </br>
Step2: Go to file and select new file option </br>
Step3:Type the program </br>
Step4:Go to file and select save option to save the program </br>
Step5:Go to sketch and select verify or compile options </br>
Step6:If no error Hex file will be generated in the temporary folder </br>
### Proteus
Step7:Open the Proteus software </br>
Step8:Go to file select new design and click ok button </br>
Step9:Select component mode and click pick devices from the library </br>
Step10:Type the component name in the keyword to select the components and click ok button </br>
Step11:Design the circuit as per the diagram </br>
Step12:Double click the Arduino controller and upload the hex file generated by Arduino IDE </br>
Step13:Click start button and check the output

## THEORY:
Servo Motor Theory There are some special types of applications of an electric motor where the rotation of the motor is required for just a certain angle. For these applications, we require some special types of motor with some special arrangement which makes the motor rotate a certain angle for a given electrical input (signal). For this purpose, servo motor comes into the picture.

![image](https://github.com/charan07gr/Servo-Motor-Interfacing/assets/132322854/4d3a3306-3efc-43d0-b07f-994ac255efdd)


The servo motor is usually a simple DC motor controlled for specific angular rotation with the help of additional servomechanism (a typical closed-loop feedback control system). Nowadays, servo systems are used widely in industrial applications.

Servo motor applications are also commonly seen in remote-controlled toy cars for controlling the direction of motion, and it is also very widely used as the motor which moves the tray of a CD or DVD player. Besides these, there are hundreds of servo motor applications we see in our daily life.

The main reason behind using a servo is that it provides angular precision, i.e. it will only rotate as much we want and then stop and wait for the next signal to take further action. The servo motor is unlike a standard electric motor which starts turning as when we apply power to it, and the rotation continues until we switch off the power. We cannot control the rotational progress of electrical motor, but we can only control the speed of rotation and can turn it ON and OFF. Small servo motors are included many beginner Arduino starter kits, as they are easy to operate as part of a small electronics projects.

## PROGRAM:
#include <Servo.h> </br>
Servo myservo; </br>
int pos = 0; </br>
void setup() </br>
{ </br>
myservo.attach(4); </br>
} </br>
void loop() </br>
{ </br>
for(pos = 0; pos <= 180; pos += 1) </br>
{ </br>
myservo.write(pos); </br>
 </br>
delay(15); </br>
 </br>
} </br>
for(pos = 180; pos>=0; pos-=1) </br>
 </br>
{ </br>
 </br>
myservo.write(pos); </br>
 </br>
delay(15); </br>
 </br>
} </br>
} </br>

## CIRCUIT DIAGRAM:
![image](https://github.com/charan07gr/Servo-Motor-Interfacing/assets/132322854/e142c4dc-4be6-4d8d-b6f3-1bef03e0737f)

## OUTPUT:
![image](https://github.com/charan07gr/Servo-Motor-Interfacing/assets/132322854/c9b17db3-2031-4477-b6d5-35dcce664c90)

## RESULT:
Thus the speed and direction of the servomotor was controlled using Arduino UNO controller.
