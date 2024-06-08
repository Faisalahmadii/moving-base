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
•	Arduino Mega 2560
•	HC-SR04 Ultrasonic Sensor
•	Motor Control Shield
•	ESP8266
•	DC Motor & Wheels

	## Software:
•	Arduino IDE
•	User interface
•	MQTT.fx

# Flowchart:

## Mod 1&2:
 ![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/9f2dad15-d84b-491c-a8b6-4db3a3ecfd9b)

## Mod 3:
![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/0f28d118-48a8-4a41-bd97-006f96cdc0b8)
 
# Sequence diagrams:

The sequence diagram for the Moving Base Project details the interactions and processes within three modes: User-Controlled, Autonomous, and Grid-Based Navigation. In User-Controlled Mode, a user sends commands that Node-RED publishes, the MQTT Broker transmits via MQTT, the ESP8266 forwards, and the Arduino executes (move forward, backward, turn left, turn right). In Autonomous Mode, ultrasonic sensors read data sent to the Arduino, which checks for obstacles and adjusts the path accordingly. In Grid-Based Navigation Mode, the user enters coordinates that Node-RED publishes, the MQTT Broker transmits via MQTT, the ESP8266 forwards, and the Arduino calculates the target position, adjusting the path based on sensor data and moving to the target position while avoiding obstacles. 
![image](https://github.com/Faisalahmadii/moving-base/assets/170818993/10c70b9f-cc98-46e9-be48-d942bfc813a3)



