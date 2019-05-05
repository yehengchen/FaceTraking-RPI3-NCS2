# Pan/tilt face tracking with a Raspberry Pi + NCS
*This project using the NCS with openvino and ServoBlaster to drive*
multiple servos via the GPIO pins
to face tracking
### Demo video is shown [[YouTube]](https://www.youtube.com/watch?v=n2YM4_2WDlU)

<img src="https://github.com/yehengchen/FaceTracking-RPI3-NCS/blob/master/img/b4lvt-8lfrb.gif" width="50%" height="50%">

## Installation Python Libraries:
* Python 3.5
* Picamera
* OpenVINO
* Numpy

## Things needed:
* A raspberry pi 3B
* A Neural Compute Stick - (NCS)
* A pan/tilt bracket - ([3D printer](https://github.com/yehengchen/FaceTracking-RPI3-NCS/blob/master/ProfileBlock_SUCPT_CamMount_28.5mm.gcode))
* Two Servos - (SG90)
* A GPIO expansion board
* Pi Camera or USB Webcam

<img src="https://github.com/yehengchen/FaceTracking-RPI3-NCS/blob/master/img/3Dprint.png" width="32%" height="32%">

*Pan-and-tilt bracket: ProfileBlock_SUCPT_CamMount_28.5mm.gcode*

## Install the OpenVINO™ Toolkit for Raspbian* OS Package
### METHOD 1:
* #### Run this script [./Install_openvino.sh](https://github.com/yehengchen/FaceTracking-RPI3-NCS/blob/master/Install_openvino.sh)
*This script provides all instructions on install the OpenVINO™ toolkit package for Raspbian* OS*
### METHOD 2:
* #### The following steps will be covered: __[[Guide]](https://github.com/yehengchen/NCS2-OpenVINO)__
*This guide provides step-by-step instructions on how to install the OpenVINO™ toolkit for Raspbian* OS*

### To test your OpenVINO, open a new terminal. You will see the following:
        
    [setupvars.sh] OpenVINO environment initialized

## Getting Started:
### Install and start multiple servos:
    git clone git@github.com:yehengchen/FaceTracking-RPI3-NCS.git
    cd FaceTracking-RPI3-NCS/ServoBlaster/user
    sudo ./servod
    
### Testing multiple servos:
    echo 0=+10 > /dev/servoblaster
    echo 1=+10 > /dev/servoblaster

### Testing Picamera:
    raspistill -o image.jpg

### Run face tracking:
    python3 pi_NCS_face_traking.py

    
## Reference:
[PiBits-ServoBlaster](https://github.com/richardghirst/PiBits/tree/master/ServoBlaster)
