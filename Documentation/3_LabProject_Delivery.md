# GEB Project tools
## 1. Introduction
In this lab session, we integrated an ESP32 sensor with a virtual robot to monitor its movement in 3D in real time. First, we prepared the workspace with the necessary tools, like Visual Studio Code and Python, and downloaded the files from GitHub.
Next, we programmed the sensor board. We uploaded the code using PlatformIO. We gave both the sensor and our computer a fixed adress (IP) so they can communicate each other.
Finally, we linked everything together. We opened the 3D model in RoboDK and ran a Python script. This script took the rotation data (Roll, Pitch, and Yaw) from the physical sensor and moved the virtual model at the same time. When we moven the sensor manually, the virtual robot moved exactly the same way on the screen.
