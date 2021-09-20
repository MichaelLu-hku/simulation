This software depends on ROS. Installation instructions can be found here. We have tested this software on Ubuntu 18.04 and ROS Melodic.

# 1. Dependencies installation

## 1.1 turtlebot related rospackage installation 
```
$ sudo apt install ros-melodic-turtlebot3*
```
## 1.2 dvs driver installation 

Please follow the instructions (steps 1-9) at [rpg_dvs_ros](https://github.com/uzh-rpg/rpg_dvs_ros)
(Pay attention that you should create another ros workspace compiled with catkin build)

# 2. Started simulation

First cd to the collume you created in 1.2, clone the project and catkin build
```
$ cd ~/catkin_ws/src
$ git clone https://github.com/MichaelLu-hku/simulation
$ cd ../ && catkin build simulation
```
you can start the simulation now:
```
$ roslaunch simulation start.launch 
```
and you can control the motion of your turtlebot by:
```
rosrun turtlebot3_teleop turtlebot3_teleop_key
```
