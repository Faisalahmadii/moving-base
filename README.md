  # INTRODUCTION:
In today's industries, transportation operations encounter numerous challenges, including the movement of goods, returning to the original point, and the transportation of heavy materials. These challenges often result in high labor costs and the need for efficient logistics services. To overcome these obstacles, we have developed an innovative IoT project that revolutionizes transportation processes.
Our project combines a mobile base, equipped with sensors, a microcontroller, and MQTT communications, to provide a versatile and efficient solution. Our primary objective is to simplify resource transportation, reduce labor costs, and facilitate the movement of heavy and bulky items.
Utilizing advanced motion algorithms, including autonomous mode, user-controlled mode, and grid-based navigation mode, our project enables the mobile base to adapt to dynamic conditions seamlessly. This intelligent mobility capability significantly enhances movement efficiency while ensuring the safe transportation of goods and resources.
The robust construction of our mobile base, coupled with a powerful motor system, empowers it to effortlessly carry substantial loads that would otherwise pose challenges for human workers. By reducing reliance on manual labor, our project contributes significantly to cost savings and enhances workplace safety.
With our IoT-based project, we address the transportation challenges faced across various sectors. By simplifying resource movement, reducing labor costs, and streamlining logistics, we drive efficiency, safety, and optimize resource utilization.
The integration of IoT technology brings real-time data, advanced algorithms, and seamless connectivity into the transportation landscape, transforming the way stores and other sectors handle their transportation operations.


# Project Overview:
Our project encompasses three distinct operational modes, each offering unique functionality and control capabilities for the moving base:

1-	User-Controlled Mode:
In this mode, users interact with the moving base through Node-RED, inputting commands that are transmitted to the Arduino via MQTT. This seamless communication pathway enables users to remotely control the base's actions and functionalities. The MQTT protocol facilitates data transmission from Node-RED to an ESP8266 module, which acts as an intermediary before forwarding commands to the Arduino for execution.

2-	Autonomous Mode:
Operating independently, the Arduino empowers the moving base to navigate its environment autonomously. Utilizing predefined algorithms, the Arduino analyzes sensor inputs, detects obstacles, and adjusts the base's path as needed, without requiring continuous external intervention. This autonomous functionality ensures smooth and efficient movement, enhancing the base's adaptability and operational efficiency.

3-	Grid-Based Navigation Mode:
In the third mode, the moving base environment is divided into a matrix grid, allowing users to specify precise destinations by entering coordinates such as [0][3]. Users input these coordinates via Node-RED, and the data is transmitted to the Arduino through MQTT and an ESP8266 module. The Arduino interprets the coordinates and navigates the base to the specified point within the matrix, providing users with precise control over the base's movement within the environment.


# Project Design and components
## Hardware Components:
1-Arduino Mega 2560
2-HC-SR04 Ultrasonic Sensor
3-Motor Control Shield
4-ESP8266
5-DC Motor & Wheels
6- power

## Software:
1-Arduino IDE
2-User interface
3-MQTT.fx

# Flowchart:

## Mod 1&2:
 ![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/9f2dad15-d84b-491c-a8b6-4db3a3ecfd9b)

## Mod 3:
![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/0f28d118-48a8-4a41-bd97-006f96cdc0b8)
 
# Sequence diagrams:

The sequence diagram for the Moving Base Project details the interactions and processes within three modes: User-Controlled, Autonomous, and Grid-Based Navigation. In User-Controlled Mode, a user sends commands that Node-RED publishes, the MQTT Broker transmits via MQTT, the ESP8266 forwards, and the Arduino executes (move forward, backward, turn left, turn right). In Autonomous Mode, ultrasonic sensors read data sent to the Arduino, which checks for obstacles and adjusts the path accordingly. In Grid-Based Navigation Mode, the user enters coordinates that Node-RED publishes, the MQTT Broker transmits via MQTT, the ESP8266 forwards, and the Arduino calculates the target position, adjusting the path based on sensor data and moving to the target position while avoiding obstacles. 
![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/10c70b9f-cc98-46e9-be48-d942bfc813a3)



# Circuit diagram:
![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/f90a0564-b60d-47c5-b2bf-7b65189292f0)

# Prototype:
![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/d5f26d26-5dc7-4783-a5d1-97abab434e7b)
 ![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/dbf266bd-c9cf-4beb-92b4-042d21a0b4b3)


 # RESULT & System model:
## Mode1(User-Controlled Mode):

![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/d7b4fc3c-5a9d-4d7c-9150-ba24f12f0932)

![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/a2c44b05-8e22-4a8f-a47b-1f0064163195)

In this figure, the user is commanding the moving base robot to move forward using a control panel on Node-RED displayed on a phone, directing the moving base robot to advance in User-Controlled mode. The robot responds to this input by moving forward, 

![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/c51b55a8-e012-4c5a-9bb3-187f76f82c5e)

The user now selects the "Right" command on the Node-RED control panel, directing the robot to turn right.


## MODE2 (Autonomous Mode):

![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/9b8f2d29-7994-474c-ad36-5b273278e74b)

![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/c735a520-4ccf-48e9-a70f-48b89a7073f3)

 In this image, the moving base robot is shown in Autonomous mode, where it has encountered an obstacle directly in its path. This situation highlights the robot's capability to detect and respond to obstacles in its environment autonomously
 
 ![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/d37cbe6f-ffd6-4cf5-8f75-32b44006cfe7)
 
 After detecting an obstacle, the moving base robot uses its left and right sensors to read distances. It then moves toward the direction with the higher distance value.
then the moving base robot continues to proceed, 

## Mode 3 (Grid-Based Navigation Mode):

![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/fb17913e-36c6-4912-8bcb-55994c197733) 

![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/3aee14cb-2c60-496c-98ff-8ce136e7ddff)

![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/01e89621-7122-4277-a513-b42091c484fc)

 ![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/bf6fbbf3-d23e-499e-8eec-bba6fb779786)

  ![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/45ed3b53-5195-45ca-b9a2-05f5ca694477)


# How to construct the matrix and dimensions(Mod 3):

This image is a schematic representation of a grid-based navigation system for a car within a room. The diagram includes the car's dimensions, room dimensions, and the calculation for the number of blocks in the grid. Here's a detailed explanation of each component in the diagram: Diagram Components:

1.   Car Dimensions:
   
Car Length (L): 0.42 meters

Car Width (W): 0.42 meters

2.  Room Dimensions:
   
Room Length (RL): 2.10 meters

Room Width (RW): 2.10 meters

3.  Grid Representation:
   
The room is divided into a grid based on the car's dimensions. Each block in the grid represents a space that can fit the car.

4.  Grid Calculations:
   
R (Number of Rows): Calculated by dividing the room length (RL) by the car length (L).

R=RLL=2.100.42=5

C (Number of Columns): Calculated by dividing the room width (RW) by the car width (W).'

C=RW/W=2.10/0.42=5

5.   Speed and Time Calculations:
   
S (Speed): Represented as distance divided by time

S=d/t

B (Time for One Block): The time it takes for the car to move one block in the grid.

B=CarW/S

B=CarL/S


