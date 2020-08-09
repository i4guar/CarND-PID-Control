# PID Control
As part of the Self-driving nanodegree programm I have written a PID Controller in C++. To test the controller a simulator was provided by udacity.

Here the [project](https://github.com/udacity/CarND-PID-Control-Project) with the starter code and project instruction.


[//]: # (Image References)

[simulator]: ./res/simulator_image.png "Simulator"

## Simulator

The car is able to drive around the track by using the PID Controller.

Here the [short video](./res/simulator_recording.mov) of the car driving on the track.

This image shows how the car is approximately centered on the road:
![alt text][simulator]

## Reflections

My approach was to implement the PID controller and then to customize the parameters of it manually to get a feel for what happens when the parameters change.

Here my observations:
* The hardest part was to make the car take the sharper turns at the end of the track as a higher steering angle was need. As the car didn't have any foresight it was not possible to prepare for a sharp turn properly.

* The P-value (0.1) is very relevant for how much the vehicle oscillates around the target trajectory. If the target was to high the car overshoots and if the value is to low the car was not able to make a sharp turn. I tried to make it as small as possible while still being able to make a steer sharp.

* The impact of the I-value (0.0005) was much smaller than I expected. If it was to high the car was not able to follow the target line, but it felt for me like that a very small value improved the oscillation around the center.

* The D-value (0.75) influenced how erratic the vehicle behaved. When to high the car made very sudden movements and when to low the car overshoot the target as the P-value dominated. 

With the right combination I finally managed to get the vehicle around the track.