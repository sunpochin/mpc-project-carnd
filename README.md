# CarND-Controls-MPC
Self-Driving Car Engineer Nanodegree Program

## Overview 
Model Predictive Control

---

## Rubric Points
---
### Compilation
---
#### Your code should compile.
> Code must compile without errors with cmake and make.

> Given that we've made CMakeLists.txt as general as possible, it's recommend that you do not change it unless you can guarantee that your changes will still compile on any platform.

---
### Implementation
---
#### The Model
> Student describes their model in detail. This includes the state, actuators and update equations.

#### Timestep Length and Elapsed Duration (N & dt)
> Student discusses the reasoning behind the chosen N (timestep length) and dt (elapsed duration between timesteps) values. Additionally the student details the previous values tried.



#### Polynomial Fitting and MPC Preprocessing
> A polynomial is fitted to waypoints.

> If the student preprocesses waypoints, the vehicle state, and/or actuators prior to the MPC procedure it is described.


#### Model Predictive Control with Latency
> The student implements Model Predictive Control that handles a 100 millisecond latency. Student provides details on how they deal with latency.



### Simulation
---
#### The vehicle must successfully drive a lap around the track.
> No tire may leave the drivable portion of the track surface. The car may not pop up onto ledges or roll over any surfaces that would otherwise be considered unsafe (if humans were in the vehicle).

> The car can't go over the curb, but, driving on the lines before the curb is ok.




## Installation (copied from original)
Installation instruction from Udacity repository: [link](https://github.com/udacity/CarND-MPC-Project/blob/master/README.md)

