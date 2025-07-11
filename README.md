
---

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github.com/ManchesterRoboticsLtd/Puzzlebot/blob/main/Misc/Logos/Puzzle_Bot_Logo_W.png">
  <source media="(prefers-color-scheme: light)" srcset="https://github.com/ManchesterRoboticsLtd/Puzzlebot/blob/main/Misc/Logos/Puzzle_Bot_Logo_B.png">
  <img alt="Shows MCR2 logo in black or white." width="250" align="right">
</picture>


 <div id="user-content-toc">
  <ul align="center" style="list-style: none;">
    <summary>
      <h1>Puzzlebot NVIDIA JETSON® Edition</h1>
    </summary>
  </ul>
</div>

---

## Introduction

* The Puzzlebot NVIDIA JETSON® Edition is an extension of the Puzzlebot Hacker Edition.
* Developed alongside NVIDIA, combining the power of the Hackerboard and the NVIDIA JETSON Nano®


<p align="center">
  <img src="https://github.com/user-attachments/assets/edd9ea01-ecbc-4fe1-9ce1-c9affd19c339" alt="Shows Puzzlebot views in black or white." width="650">
</p>

* Allows users to implement research-level, real-time algorithms such as AI & Computer Vision, SLAM and 
autonomous driving algorithms using ROS.

* Ideal for control, advanced robotics, computer vision and AI tasks.

* Puzzlebot Jetson Edition includes all essential components to develop from basic control to advanced robotics algorithms.

* Designed to accompany you in your robotic applications or during the MCR2 digital curriculum.

---

## 🚀 Features

- 🔧 **Differential drive base** with encoder feedback  
- 🧠 **Jetson Nano** (4-core ARM CPU + GPU for AI acceleration)  
- 📷 **Raspberry Pi Camera (CSI)**  
- 📡 **Time-of-Flight (ToF) distance sensor**  
- 🌀 **Servo motor** for pan TOF scanner  
- 🧩 Modular architecture with Hackerboard electronics  
- 🌐 ROS 2 (Humble) compatible  
- 🖥️ Optional Gazebo/ROS 2 simulation support  
- 🔌 Supports additional sensors (IMU, LiDAR, etc.)

---

## Configurations
### Puzzlebot-ROS Connection: Classic 
* The user can develop advanced robotic algorithms in ROS (Robot Operating System) using the computing power of the NVIDIA Jetson Nano® and communicate to the actuators and sensors using the Hackerboard.
* The Hackerboard and NVIDIA Jetson Nano® are connected via Serial (Communication Libraires with Hackerboard, Sensors and Actuators, provided by MCR2).



<p align="center" >
  <img src="https://github.com/user-attachments/assets/0283afef-7beb-42ae-ba6a-f23b684af5a6"  width="600"/>
</p>


### Puzzlebot-ROS Connection: Client
* In tis configuration, the user can connect to the NVIDIA Jetson Nano®, to monitor the functionality of the robot, monitor or control a process or simply control the robot wirelessly.
* This configuration works as the previous one, with the difference that in this case the user can connect to the External computing unit (ROS Master) via Wi-Fi.
* The ROS Master node is running in the NVIDIA Jetson Nano® making this a suitable combination for Advanced Distributed Control.


<p align="center" >
  <img src="https://github.com/user-attachments/assets/27e62a75-fcc9-4953-9786-ef8389449ef4"  width="700"/>
</p>

## General Information
  * NVIDIA Jetson Nano works with an image based on Ubuntu 22.04
  * The ROS Version installed on the MCR2 Jetson Image is ROS2 Humble.

## Instructions
1. Install the latest Hackerboard Binaries, if not previously installed, install them following the instructions in the folder *MCR2_Hackerboard_Binaries*

2. Flash the MCR2-Jetson Nano Image to the SD Card.
   * Download the NVIDIA Jetson Nano Image
     * [Jetson Nano 2GB](https://manchesterrobotics-my.sharepoint.com/:u:/g/personal/mario_mtz_manchester-robotics_com/EVMUSVxzaepInxdKvzXnhpQBFf7i77sH-8Dk36olx9yuzg?e=26PTBO)
     * [Jetson Nano 4GB](https://manchesterrobotics-my.sharepoint.com/:u:/g/personal/mario_mtz_manchester-robotics_com/EXvVxs2Mb4FMh8F7bGicvkoBsSl_ZeBqURtW6L4Tzr2_kQ?e=iVcIMZ)
  * Use the Balena Etcher to flash the image [here](https://www.balena.io/etcher)
  * More information can be found in the presentation *MCR2_Puzzlebot_Jetson_Ed_ROS2.pdf*
  
3. Access the Hackerboard *Web Interface* (More in depth explanation can be found in the Manual *MCR2_Puzzlebot_Jetson_Ed_ROS2.pdf*)
  * Select the Network (![image](https://user-images.githubusercontent.com/67285979/232577316-c4c3cddf-99aa-4d03-9480-7fc041363f07.png)
 ) icon on the taskbar. The icon that appears depends on your current connection state. If you don’t see one of the network icons (or a similar one) shown in the following image, select the Up arrow (^) to see if it appears there.
  * Choose the Puzzlebot Wi-Fi network of the robot you want (Puzzlebot x), then select Connect.
  <p align="center" >
  <img src="https://user-images.githubusercontent.com/67285979/232576490-467fe6e9-724d-4d78-9007-12bd5c59dcb0.png"  width="300"/>
  </p>
  
  * Type the network password as shown on the LCD Display, and then select Next.
  
  <p align="center" >
  <img src="https://user-images.githubusercontent.com/67285979/232577617-646995cb-b484-4635-ab54-eb137c1087f5.png"  width="400"/>
  </p>
  
  * Connect to the AP of the Hackerboard 

  *	Open any web browser

  <p align="center" >
  <img src="https://user-images.githubusercontent.com/67285979/232574285-d4d5a6a5-0df9-43c8-a4ef-f2f7ef97af0b.png"  width="200"/>
  </p>
    
  * Type in the search bar (address bar) the IP Address of the robot as displayed on the LCD screen.
  <p align="center" >
  <img src="https://user-images.githubusercontent.com/67285979/232574380-db697767-4d95-4468-b4c9-b83883a88e0e.png"  width="500"/>
  </p>

  * The following webpage should appear. 
  <p align="center" >
  <img src="https://user-images.githubusercontent.com/67285979/232581339-03e1545d-a330-47b5-9a02-2ec6314e16dd.png"  width="500"/>
  </p>
  
  * Make sure the ROS Checkbox is selected and select the type of control for your robot (The ROS topic will change accordingly).
      * Robot Velocitites (Activates the internal PID control for the linear and angular velocities of the robot)
      * Wheel Velocitites (Activates the internal PID control for the independent angular speed of the wheels)
      * Motor PWM (Directly input the PWM value [-1,1] to the motor driver)
  * Press the "Save" button for each selection
  <p align="center" >
  <img src="https://user-images.githubusercontent.com/67285979/232582025-a5180e7a-586f-4d22-a850-845de9e612af.png"  width="500"/>
  </p>
  
  4. Configure the Jetson (in case you have multiple robots at once) as shown in the presentation *MCR2_Puzzlebot_Jetson_Ed_ROS2.pdf*
  
  5. Connect the Hackerboard using the included USB-microUSB cable.
      * If using another cable make sure is a Data-Cable not a Power-Cable

  <p align="center" >
  <img src="https://user-images.githubusercontent.com/67285979/232567615-2c5bc3eb-e559-489a-97d1-c1a2513da436.png"  width="350"/>
  </p>
  
  6. Connect the Jetson to a screen, mouse, and keyboard.
  7. Ensure the Hacker Board is connected to the battery using the power cable and booted.
  8. Connect the USB-C port of the Jetson to a battery pack (can be the same as the hackerboard)
    - Other USB power sources work but the Jetson draws up to 3A of current and may crash if the power supply cannot provide this
  9. Once the Jetson has booted, you should see the Jetson Desktop.

  <p align="center" >
  <img src="https://user-images.githubusercontent.com/67285979/232599153-740b3dd7-03db-45f9-abba-cea1a0f67595.png"  width="350"/>
  </p>
  
### Hackerboard Communication Routines
* The Hackerboard communication needs to be launched each time the jetson is booted using the following comand on the LXT Terminal of the Jetson (see *MCR2_Puzzlebot_Jetson_Ed_ROS2.pdf*)
```
ros2 launch puzzlebot_ros micro_ros_agent.launch.py
```
* To test the communication, use rostopic list. You should see  list of topics as shown, although this will depend which control mode the Hacker Board is using. 
  
### Testing Routines
* Test the ROS communication with rostopic echo
* Echo the topics /VelocityEncL and /VelocityEncR, and rotate the wheels
* The speed of the wheels should be displayed

* Publish to the command topics defined on the Hackerboard web interface, the wheels should turn
  - If Robot Velocitites mode is used, publish to /cmd_vel
  - If Wheel Velocitites is used, publish to /VelocitySetR and /VelocitySetL
  - If Motor PWM is used, publish to /ControlR and /ControlL

### Remote access
* To control the robot remotely, follow the steps in the presentation.
* Do the Teleoperation activity.


