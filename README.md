# Model Predective Control

Model Predective Control (MPC) is implemented to drive the car autonmously on the track, which is done as part of udacity self driving car engineer nano degree(https://www.udacity.com/drive).

![mpc animation](images/Model_Predictive_Control.gif)

for Result [check](https://www.youtube.com/watch?v=TeZY0GmgeAM&feature=youtu.be)

### Approach
For model predicitve model control, I used the simple kinematic model with the model state consiting of following parameters

* x position
* y position
* velocity
* orientation
* cross track error
* orientation error

The control action is on 2 actuators
* steering angle
* acceleration 

The following image shows the state and the update equations:
![equations](images/equations.png)

The MPC computes the cross track error (cte) and orientation error based on the state, then minimizes the cost function based on the constraints and the controller computes the optimal desired steering angle and throttle which makes the car to drive on the road keeping the car to center of the road.


