# Object-tracking-algorithms
These are a collection of algorithms which can be efficiently used to track objects in a picture as per user's choice. In the python programs, I have tried to present total 8 ways in which objects in your camera frame can be tracked. These algorithms do not involve any AI/ML knowledge to use so if you're a newbie and not good at them, this is for you !

[![Made with Python](https://img.shields.io/badge/Made%20with%20-Python-yellow?style=for-the-badge&logo=python)](http://www.cplusplus.com/)
[![LinkedIn-profile](https://img.shields.io/badge/LinkedIn-Parthsarthi-blue?style=for-the-badge&logo=LinkedIn)](https://www.linkedin.com/in/parthsarthi-gupta-265b9816a)
[![Python](https://img.shields.io/badge/Python-version%203.7.5-green?style=for-the-badge&logo=Python)](http://www.python.org)
[![OpenCV 4.3.0](https://img.shields.io/badge/Framework-OpenCV-orange?style=for-the-badge&logo=data:png;base64,)](https://pypi.org/project/opencv-python/)

### Cloning
Use the link below to clone this repository to your machine.
```
https://github.com/Severus11/Object-Tracking-Algorithms.git
```
### Pre-requisites 
These are the required dependencies needed to setup the environment
```
$ pip3 install opencv-python==4.3.0
$ pip3 install opencv-contrib-python
```
### How to use:
- Install the requirements.txt file and run the desired python file.
- Input the algorithm you want to use for motion tracking.
- An initial frame will pop up. Select the object to be tracked.
- Observe and enjoy moving the object around your screen.

### Which tracking API to chose?
#### 1. Booster Tracking 
- Based on the same algorithm used to power the machine learning behind Haar cascades (AdaBoost), but like Haar cascades, is over a decade old. This tracker is slow and doesn’t work very well. Interesting only for legacy reasons and comparing other algorithms. (minimum OpenCV 3.0.0)
#### 2. MIL Tracking
- Better accuracy than BOOSTING tracker but does a poor job of reporting failure. (minimum OpenCV 3.0.0)
#### 3. KCF Tracking
- Kernelized Correlation Filters. Faster than BOOSTING and MIL. Similar to MIL and KCF, does not handle full occlusion well. (minimum OpenCV 3.1.0)
#### 4. TLD Tracking
- TLD tracker was incredibly prone to false-positives. Idk if it is the algorithm or the actual implementation. If you find do make a PR !
#### 5. MedianFlow Tracking
- Does a nice job reporting failures; however, if there is too large of a jump in motion, such as fast moving objects, or objects that change quickly in their appearance, the model will fail. (minimum OpenCV 3.0.0)
#### 6. GoTurn Tracking
- This tracker is deep learning based. It requires additional model files to run. Initial experiments showed it was a bit of a pain to use even though it reportedly handles viewing changes well.
#### 7. Mousse Tracking
- Very, very fast. Not as accurate as CSRT or KCF but a good choice if you need pure speed.
#### 8. CSRT Tracking
- Discriminative Correlation Filter (with Channel and Spatial Reliability). Tends to be more accurate than KCF but slightly slower. (minimum OpenCV 3.4.2)


#### My personal suggestion is to:

- Use CSRT when you need higher object tracking accuracy and can tolerate slower FPS throughput.
- Use KCF when you need faster FPS throughput but can handle slightly lower object tracking accuracy.
- Use MOSSE when you need pure speed.

### Author
 [![LinkedIn-profile](https://img.shields.io/badge/LinkedIn-Parthsarthi-blue.svg)](https://www.linkedin.com/in/parthsarthi-gupta-265b9816a)

- Parthsarthi Gupta
