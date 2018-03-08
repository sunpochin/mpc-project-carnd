# CarND-Controls-MPC
Self-Driving Car Engineer Nanodegree Program

## Overview 
Model Predictive Control

## Result video
---
https://youtu.be/vuNA2bOWKP0

## Rubric Points
---
### Compilation
#### Your code should compile.
> Code must compile without errors with cmake and make.

It compiles on my ubuntu 16.04 laptop without warning and error. 

### Implementation
#### The Model
> Student describes their model in detail. This includes the state, actuators and update equations.

This project uses a Kinematic model, which is a simplification of dynamic model that ignore tire forces, gravity, and mass.

The model consists 4 States, 2 Control Inputs, and 2 Errors.

##### States:
* x and y are the coordinates of the vehicle. <br>
* ψ is the orientation of the vehicle. <br>
* v is the velocity of the vehicle. <br>

##### Control Inputs:
The states of the next time step can be calculated at the next time step with the following equations:
* x(t+dt) = x(t) + v(t) ∗ cos(ψ(t)) ∗ dt
* y(t+dt) = y(t) + v(t) ∗ sin(ψ(t)) ∗ dt
* ψ(t+dt) = ψ(t) + (v(t)/Lf) ∗ δ(t) ∗ dt
* v(t+dt) = v(t) + a(t) ∗ dt

##### Errors and Cost Function:
Cross Track Error (cte) and Psi Error (eψ) are used to build the cost function of the model. They are calculated at the next time step with the following equations:
* cte(t+dt) = cte(t) + v(t) ∗ sin(eψ(t)) * dt
* eψ(t+dt) = eψ(t) + (v(t)/Lf) ∗ δ(t) ∗ dt


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

