# **CarND-PID-Control-Project** 

---

**CarND PID Control Project**

The goals / steps of this project are the following:
* Implement a PID Controller to control car in simulator
* Test on simulator that the car stays on track
* Summarize the results with a written report


[//]: # (Image References)

[image1]: ./image1.jpg "Driving car"

---
### Files Submitted 

The following files were changed during the implementation:
* main.cpp contains car driving logic
* PID.cpp  contains PID controller logic


#### 1. Project Basics

In this project the C++ was used to program. The project goal is to drive a car around circular track that has sharp left and right turns. Car need to take left and right turns without touching or running over the edges of the lane. 
The simulator measures cross-track error between the lateral position of the car and the center of the lane and sends it to PID Controller
and receives the steering angle and the throttle.


#### 3. Accuracy

The PID Controller parameters were choosen on two steps, first the twiddle algorithm was used to get approximate coefficients,  then these coefficients were tuned manually. The final coefficients were Kp=0.13, Ki=0, Kd=2.3

Accuracy was tested using Udacity simulator

![alt text][image1]
