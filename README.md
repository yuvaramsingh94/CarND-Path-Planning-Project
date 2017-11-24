# CarND-Path-Planning-Project

### About this project

path planning project provided by Udacity for the Self driving car term 3 mainly focus on the implementation of path planner for autonomous car on highways . Udacity provides the student with a simulator and started code (c++) to get started with this project . the main aim of the project is to make the car navigate around the simulated highway with traffics safely . the important task here is to make our car navigate dense traffic with ways to change lane if we are tailing a slow car . this serves as a place to tryout predictions,usage of sensor fusion values , behaviour planner,trajectory generator . etc

### My solution

For my implementation i used the methods stated on the walkthrough video provided to create the smooth trajectory. i implemented a finite state machine like approach with basic change lane left ,change lane right , keep lane ,prepare change lane states. my model calculates the relative position of the car in front of it with our car , if it detects a collision (if both cars s value are within certain distance ) then it chicks for lane change possibilities . Note : i have not implemented any cost functions yet .

#### Lane change

My implementation check for lane shift if the car we are tailing is going slow . it checks for the traffic cars S value on the intended lane . if there is a safe situation to make the lane change (no cars  , or car is in safe distance ) the algorithm will change the lane value which in turn generates a new trajectory to safely change lane

#### Future enhancement

1. implementation of prediction to determine future positions of traffic cars
2. implementation of cost functions . now we are just using if else based decision making steps
3. implementation of search algo to predict the best trajectory with minimal jerk and acceleration

#### code explanation

* in main.cpp:66 - definition of lane change function to check the lanes for dangerous cars
* in main.cpp:403 - implementation of transition functions


