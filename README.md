The purpose of this project is to control the movement of three simulated robots using ROS and Gazebo, so that each robot reaches its designated flag as quickly as possible. The robots have the capability to track their position and orientation within the simulation. In this project we want to move the robot to the appropriate flag, using diffrent approaches.
Files which contains our implementation are:

Our project is to move three simulated robots from a starting position to the adequate flag without any collision with another robot. The first robot should move to flag1, second robot move to flag2, and third robot to flag3. The robots have to reach the adequate flag as fast as possible.
The simulated robots are defined as follow: 
- An ultrasonic sensor is embedded, with a limited range (5 meters) 
- 2 motorized wheels allow the robot to operate in the environment 
- Its current pose in the environment is known (Position and orientation)

Our project contains four main files:
• agent.py – solution for timing
• agent_PID.py - solution of controlling the velocity
• agent_PID_2.py- solution of PID controller strategy
• agent_angular.py – solution for angular strategy

PID strategy:
This implementation uses a PID controller to control the robot's linear velocity based on the distance to the flag. The desired distance from the flag is set as a class attribute, and the proportional, integral, and derivative gains are also set as class attributes. The run_demo function then uses these values to calculate the output of the PID controller and set the robot's linear velocity. The robot will stop when it reaches a distance less than 0.9 from the flag.
Angular strategy:
The new strategy that we've provided is a simple approach for controlling the robot's movement based on the distance to the flag. The robot's angular velocity is adjusted based on the distance to the flag, with the robot turning more sharply as it gets closer to the flag. When the distance to the flag is less than 2.3, the robot stops moving. The robot moves forward at a constant linear velocity of 1.8.
