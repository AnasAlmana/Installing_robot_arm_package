# Installing_robot_arm_package
## The steps to install robot arm package and RIVz.


1-Open new terminal.

2-Create a new folder with the name `catkin_ws`, inside it create a folder named `src`. We do it by this command:
```
mkdir -p ~/catkin_ws/src
```
3-change directory to the `catkin_ws` folder that we just created.
```
cd ~/catkin_ws/
```
then 
```
catkin_make
```
```
cd ~/catkin_ws/src
```
4- Download the packages insdie `catkin_ws/src` folder:
```
git clone https://github.com/smart-methods/arduino_robot_arm.git 
```
then
```
cd ~/catkin_ws
```
```
rosdep install --from-paths src --ignore-src -r -y
```
```
sudo apt-get install ros-noetic-moveit
```
```
sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
```
```
sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
```
```
sudo apt-get install ros-kinetic-ros-controllers ros-noetic-ros-control
```
Now we need to edit the file `bachrc` and add the source to the end of this file:
```
sudo nano ~/.bashrc
```
at the end of the file add this line:
```
source /home/wesam/catkin_ws/devel/setup.bash
```
Hit `ctrl + o` to save the changes and write this command:
```
source ~/.bashrc
```

Now we can launch RIVz by this command:
```
roslaunch robot_arm_pkg check_motors.launch
```


![RIVz](https://user-images.githubusercontent.com/80279479/180818486-e64991f2-23d6-4048-aef3-98b03b8e31b0.png)

