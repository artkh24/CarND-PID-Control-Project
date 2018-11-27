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

#### 2. Description of effect each of the  P, I, D compontents in implementation

* The proportional P part of controller tries to drive car along the center line like sinusoid and if using only the P coefficient very   quickly the amplitude is geting higher and the car go out of track.
* The integral I part of controller tries to drive car in circles. In our case the I controller is equal to 0
* The differential D Part of controller tries to drive car along the curvature of track and it helps to smooth the P controller center     line overshooting


#### 3. Accuracy

The PID Controller parameters were choosen on two steps, first the twiddle algorithm was used to get approximate coefficients,  then these coefficients were tuned manually. The final coefficients were Kp=0.13, Ki=0, Kd=2.3

Accuracy was tested using Udacity simulator

![alt text][image1]
