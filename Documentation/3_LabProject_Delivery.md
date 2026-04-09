# GEB Project tools
## 1. Introduction
In this lab session, we integrated an ESP32 sensor with a virtual robot to monitor its movement in 3D in real time. First, we prepared the workspace with the necessary tools, like Visual Studio Code and Python, and downloaded the files from GitHub.

Next, we programmed the sensor board and we uploaded the code using PlatformIO. We gave both the sensor and our computer a fixed adress (IP) so they can communicate each other.

Finally, we linked everything together. We opened the 3D model in RoboDK and ran a Python script. This script took the rotation data (Roll, Pitch, and Yaw) from the physical sensor and moved the virtual model at the same time. When we moven the sensor manually, the virtual robot moved exactly the same way on the screen.

## 2. Session questions

1) **Is the plane 3D object in roboDK moving properly?**

Initially, the plane 3D object in RoboDK did not move correctly. While the communication bridge was established, the orientation was misaligned with the physical movements of the Endo-module. To fix this, we had to manually adjust the reference axes within the software to ensure that the sensor's coordinate system matched. Once the axes were properly aligned, the real-time synchronization worked as expected.


2) **What you have made to properly verify the orientation angles Roll, Pitch and Yaw?**

To ensure the accuracy of the Roll, Pitch, and Yaw (RPY) angles after our initial adjustments, we performed a verification by physically rotating the Endo-module along the  axes X (for North), Y (for side-to-side), and Z (for gravity). During this process, we did not modify the Python script; we focused on the RoboDK simulator to verify that the virtual object reacted correctly to the movements. 

3) **What you have to change in the python code when changing the plane to the needle?**

To change the 3D orientation tracking from the plane to the surgical_needle, we had to modify the Python script. We located the object_NAME variable within the Receive_data_RPY_IMU_world.py script and updated its string value from "plane" to "surgical_needle". 

## 3. Conclusions

This lab practice allowed us to obtain a new understanding on how to turn physical movement or stimuli (such us as the light turning on and off) into the digital world. 

1) **Key Learnings:** We gained experience in using ESP32 microcontrollers, managing library dependencies in PlatformIO (such as the IMU_Robotics_UB library), and using Python as a connector of hardware with simulation software.

2) **Project Applications:** These tools are highly relevant for our upcoming avant-projecte and TFG (Final Degree Project). The ability to create a "Digital Twin" of a medical instrument, allows for safer testing and better development of robotic procedures. It was especially interesting in our case, given that for our project we are planning on using ESP3 microconrollers, so gaining experience on how it works was a key point for us.

3) **Engineering point of view:** In future engineering projects, the workflow used in this practice (Git for collaboration, PlatformIO for firmware, and RoboDK for visualization) can be applied to any field requiring real-time motion tracking, such as prosthetics, industrial automation, or human-machine interfaces.
