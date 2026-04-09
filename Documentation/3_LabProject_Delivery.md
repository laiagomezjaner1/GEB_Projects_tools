# GEB Project tools
## 1. Introduction
In this lab session, we integrated an ESP32 sensor with a virtual robot to monitor its movement in 3D in real time. First, we prepared the workspace with the necessary tools, like Visual Studio Code and Python, and downloaded the files from GitHub.

Next, we programmed the sensor board. We uploaded the code using PlatformIO. We gave both the sensor and our computer a fixed adress (IP) so they can communicate each other.

Finally, we linked everything together. We opened the 3D model in RoboDK and ran a Python script. This script took the rotation data (Roll, Pitch, and Yaw) from the physical sensor and moved the virtual model at the same time. When we moven the sensor manually, the virtual robot moved exactly the same way on the screen.

## 2. Session questions

1) **Is the plane 3D object in roboDK moving properly?**
Initially, the plane 3D object in RoboDK did not move correctly. While the communication bridge was established, the orientation was misaligned with the physical movements of the Endo-module. To fix this, we had to manually adjust the reference axes within the software to ensure that the sensor's coordinate system matched. Once the axes were properly aligned, the real-time synchronization worked as expected.
![question1]("C:\Users\laiag\Pictures\Screenshots\Captura de pantalla 2026-04-09 094225.png")


3) **What you have made to properly verify the orientation angles Roll, Pitch and Yaw?**

4) **What you have to change in the python code when changing the plane to the needle?**

