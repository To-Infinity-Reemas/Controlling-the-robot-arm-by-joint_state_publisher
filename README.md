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
##### it's the line with orange high light


