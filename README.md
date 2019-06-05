## Credit

Strictly for educational usage and done for CMPE 297 Autonomous Driving class.

Used LGSVL lanefollowing application as a docker shell and updated existing code and ML models to perform object detection instead of lane tracking.

Credit and thanks to LG for providing this sample application as well as the LGSVL simulator that was used.


## Object Detection

* Uses YOLOv2 and Tiny YOLOv2 from Darknet converted to keras using yad2k library for object detection.
* Takes images from LGSVL Simulator using ROS bridge to subscribe to LGSVL node from main camera.
* Detects all objects at near real time(slow processing so images aren't smooth enough for video) in a seperate CV2 window.
* Uses frameworks/tools like Docker, Linux, ROS, LGSVL Simulator, etc.
* Performs live object detection on simulator feed. e.g. 

![Driving Objects Detection](https://i.imgur.com/bxeSLcI.png "Simulator Object Detection YOLO")

![Driving Objects Terminal](https://i.imgur.com/ZkikbRG.png "Terminal Object Detection YOLO")


To build ROS2 packages:

```
docker-compose up build
```

Now, launch the lane following model:

```
docker-compose up drive
```


## Prerequisites

- Docker CE
- NVIDIA Docker
- NVIDIA graphics card (required for training/inference with GPU)
- Linux



Uses shell of LGSVL Lane following script:

https://github.com/lgsvl/lanefollowing
