# Controlling-the-robot-arm-by-joint_state_publisher

## step1: setup a ROS workspace (Catkin)
```
mkdir catkin_ws
```

then we can go insied our folerd 
```
cd catkin_ws/
```

now we'er gonna creat a source (make sure it it exactly src inside thr catkin work space)
```
mkdir src
```

now this command you should make sure that you are inside the catkin_ws folder (not inside the src folder) :
```
catkin_make
```
#### here a pictuer to show you the previous commend :
<img width="519" alt="arm2" src="https://github.com/user-attachments/assets/35d8d5dd-8103-41b2-9acc-6a7b5b0227e5">

## step 2
now if we run the command ``` ls ``` we see that we have two new folders (build and devel)
<img width="519" alt="arm3" src="https://github.com/user-attachments/assets/1f094895-baec-4e33-93b1-a054e78d2610">

now we will apply commend called (setup.bash)
we will need to source this (setup.bash) script if we want to be able to use the code that we have written in our catkin workspace.
the commend :  
```
source ~/catkin_ws/devel/setup.bash
```

last thing here is to run ``` gedit ~/.bashrc``` then this window will appears
<img width="555" alt="arm3 3" src="https://github.com/user-attachments/assets/6d219958-dd28-4365-ab84-d33c64e84a96">

in the end of this window at line 118 you can see the source line for our global ROS installation , 
so we will add this line  ```source ~/catkin_ws/devel/setup.bash``` 
(after) the global ROS installation
##### "it's the line with orange high light"
 now save and quit the file. you should have those two lines so you can see your global ros installation as kind of a first level, and then your custom workspace here have the second level. you need to source both the global ROS installation and your catkin workspace, so you can use your code with ROS functionalities.

 ## Installing the package arduino_robot_arm
1- start with  ```scd src``` then that commend :
```
sudo apt install git
```
<img width="519" alt="arm1" src="https://github.com/user-attachments/assets/6c13e7e9-bcee-41ff-999e-45dce010cba6">

2-```git clone https://github.com/smart-methods/arduino_robot_arm```

<img width="519" alt="arm2" src="https://github.com/user-attachments/assets/c92f0d61-f970-4731-971d-228ee55af83c">

3- now go back to the (catkin_ws) using command ```cd ..``` ,then
```
rosdep install --from-paths src --ignore-src -r -y
```
<img width="519" alt="arm3" src="https://github.com/user-attachments/assets/2c4992b7-b3b2-4606-a1c6-44b403f8b31a">

4- run the command ```sudo apt-get install ros-noetic-moveit```

<img width="519" alt="arm4" src="https://github.com/user-attachments/assets/51586b4f-94f2-4664-b9b2-5085a19fefd7">

5- run the command 
```
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
```
<img width="519" alt="arm5" src="https://github.com/user-attachments/assets/2069a090-4b0a-4ebf-b9f5-3866a47d76b3">

6-
```
sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
```
<img width="519" alt="arm6" src="https://github.com/user-attachments/assets/4f12c7ad-b689-492e-aa8b-ebd4db3b6dfc">

7-
```
sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```
<img width="519" alt="arm7" src="https://github.com/user-attachments/assets/9ad8ef75-781f-49e3-9cb0-64c4e61efce3">

8-compile the package
```
catkin_make
```
<img width="519" alt="catkin8" src="https://github.com/user-attachments/assets/e7271fc6-9946-4b2d-a1bb-540e2415e029">

## Controlling the motors

#### now we can control the motors by this commend 
- when you run this command the widows will apears

```
roslaunch robot_arm_pkg check_motors.launch
```
<img width="519" alt="cont1" src="https://github.com/user-attachments/assets/93f2ea81-8a18-4803-9e84-6a694b92ed0e">

### You can move it as you want
<img width="519" alt="hi wrist" src="https://github.com/user-attachments/assets/7c9cc58a-4978-436c-bd26-1541274aa058">
