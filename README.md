# Hand Gesture Volume Control:
![Python 3.6](https://img.shields.io/badge/Python-v3.6-green) ![Opencv-Python](https://img.shields.io/badge/OpenCv--Python-v4.5-red) ![mediapipe](https://img.shields.io/badge/mediapipe-0.8-lightgrey) ![numpy](https://img.shields.io/badge/numpy-1.20-blue) ![pycaw](https://img.shields.io/badge/pycaw-20181226-yellow)


## Table of Content
  * [Application Demo](#Application-demo)
  * [Overview](#overview)
  * [Technical Aspect](#technical-aspect)
  * [Installation](#installation)
  * [Bug / Feature Request](#bug---feature-request)
  * [Technologies Used](#technologies-used)
  * [Credits](#credits)


## Demo
![GIF](VolumeController.gif)


## Overview
This is an Elementry Volume Control App using Hand Gestures. The App has been Designed using OpenCv, Mediapipe & Pycaw which takes input using Webcam/USB-Camera and returns detection of hand gestures with certain points which are basically used for Decreasing/Increasing the volumne of the System.


## Technical Aspect
This App is divided into two part:
1. __HandTracking.py__ : This File is responsible for detecting 21 different points on our hand as shown in below Video File. All points are connected to one another and they do have some coordinate value as (x,y). Video Frames are fetched using webcam or device camera can also be used.

![GIF](HandTracker.gif)



2. __VolumeControl.py__: Building App which could control volume of the system.
    - Frames which are fetched through webcam are passed one after the other for detection.
    - Corner Coordinates (X,Y) for Thumb and index finger are taken into consideration.
    - As we can see in the above Demo, Value for thumb for point as 4 is fetched by the function.
    - Volume is controlled using the distance between those points. More the distance higher the Volume and vice-versa.

## Installation
The HandGestureController App is coded in python version 3.6, with other libraries as pycaw, mediapipe, opencv-python and numpy. If you don't have Python installed you can find it [here](https://www.python.org/downloads/). Upgrade using pip package if you are using any lower version. The dependencies are mentioned in the requirements.txt file. Go with the below mentioned command for installing them in one go.
```bash
pip install -r requirements.txt
```

## Bug / Feature Request

If you find some bug/defect or if you'd like to request a new function, feel free to do so by opening an issue [here](https://github.com/RajeshKGangwar/HandGestureVolumeController/issues).

## Technologies Used

![](https://forthebadge.com/images/badges/made-with-python.svg)

<p align="left"> <a href="https://www.w3schools.com/css/" target="_blank"></a> <img src="https://www.vectorlogo.zone/logos/opencv/opencv-ar21.svg" alt="open-cv" width="150" height="150"/> <img src="https://www.vectorlogo.zone/logos/numpy/numpy-ar21.svg" alt="numpy" width="150" height="150"/>


## Credits
- [Mediapipe](https://github.com/google/mediapipe) 
- [AndreMiras-Pycaw](https://github.com/AndreMiras/pycaw)
