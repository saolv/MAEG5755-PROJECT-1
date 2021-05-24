# Final project - 1
 ### Yixiao YANG 1155148028
# Enable Robot
## 1.Preparation
### 1.1 catkin make
First enter the workspace path, and catkin_make the work space.
```
$ cd yang_ws
$ catkin_make
```
### 1.2 
Next is sim into by launching baxter.sh
```
$ ./ baxter .sh sim
$ catkin_make
```
### 1.3 Enter into the Gazebo
```
$ roslaunch baxter_gazebo baxter_world.launch
```
## 2.Overview

In order to control Baxter's arms, the robot must be put in the 'Enabled' state. Then type conmmand in terminal to actuate robot motion.
**Note:** If an error has occurred, the robot state may need to be reset or use "*Ctrl+C*" to kill the process.

## 3.Function
This robot is single function,  can only grab the coke can from the table and put it down to the preset position.
### 3.1 Add the object model
Add the table and coke can model
```
$ roslaunch exmpl_models add_table.launch
$ roslaunch exmpl_models add_coke_can.launch
```
### 3.2 Get robot in ready position
The RViz will be launched simultaneously
```
$roslaunch baxter_launch_files baxter_object_grabber_nodes.launch
```
### 3.3 Enable robot 
 The robot will complete the grasping and placing actions and retract the arm
```
$ rosrun object_grabber example_object_grabber_action_client
```
## 4.Vedio


[Baxter Grab Coke Can.mp4](https://youtu.be/9E9d6SKMnt4)
## 5.FAQ
Q：What should I do when process stuck during the running?
A: If you encounter a stuck situation when you are running, please enter "*Ctrl+C*" in the terminal to terminate the program, and then re-enter the command to continue simulate.
