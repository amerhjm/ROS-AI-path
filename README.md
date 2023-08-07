# ROS-AI-path

# task 1: install the ROS
1- download virtual Machine 
2- download ubuntu 

3- important the ubuntu file in virtual machine 
4- open the terminal on ubuntu 
5- Install ROS Noetic 
6- make work space files
7- install packages robot arm

My sources:
1-virtual machine
https://www.virtualbox.org/wiki/Downloads

2- ubuntu 
https://ubuntu.com/download/desktop

3- install ROS and packages 
https://s-m.com.sa/ros/ros.txt

--------------------------------------------------------------------------------------------------------------------------------------

# task 2
The basic steps to learn ROS through simulation with turtlebot3 and Gazebo:

1. Install ROS: First, you'll need to install ROS on your computer. You can follow the instructions on the ROS wiki to install the version that is appropriate for your operating system.

2. Install TurtleBot3 and Gazebo: Once you have ROS installed, you can install the TurtleBot3 and Gazebo packages. 

3. Launch a simulation: Once you have TurtleBot3 and Gazebo installed, you can launch a simulation to test your code. You can do this by running a launch file that sets up the simulation environment and starts the necessary nodes.

4. Develop and test your code: With the simulation environment up and running, you can start developing and testing your ROS code. You can use tools like RViz to visualize your robot and its surroundings, and you can use Gazebo to simulate sensors like cameras and lidars.

5. Iterate and refine: As you develop your code, you can iterate and refine it based on the results of your simulations. This allows you to experiment with different algorithms and approaches without risking damage to physical robots.


## Installation:

1. Install the core dependencies for controlling the TurtleBot by executing the following command in the terminal:

```
sudo apt install ros-noetic-joy ros-noetic-teleop-twist-joy \
  ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc \
  ros-noetic-rgbd-launch ros-noetic-depthimage-to-laserscan \
  ros-noetic-rosserial-arduino ros-noetic-rosserial-python \
  ros-noetic-rosserial-server ros-noetic-rosserial-client \
  ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server \
  ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro \
  ros-noetic-compressed-image-transport ros-noetic-rqt* \
  ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-markers \
  ros-noetic-gazebo-ros-pkgs
```

2. Install the additional package for the TurtleBot's servo actuators (motors):

```
sudo apt install ros-noetic-dynamixel-sdk
```

3. Install the package that defines the main messages used by the TurtleBot to communicate with ROS:

```
sudo apt install ros-noetic-turtlebot3-msgs
```

4. Install the main TurtleBot3 package:

```
sudo apt install ros-noetic-turtlebot3
```

5. After the core installation is complete, we need to install the TurtleBot3 Simulations package from the source by cloning it from Git into Catkin Workspace:

```
cd ~/catkin_ws/src/
git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
```

6. Finally, navigate back to the root of the Catkin Workspace to run `catkin_make`:

```
cd ~/catkin_ws && catkin_make
```

7. The next step is to edit the `.bashrc` file so that the correct variables are defined every time you open a new terminal. This command adds the sourcing of the `devel/setup.bash` file so that new packages installed through apt are recognized by Catkin and your terminal:

```
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc
```

8. Next, this line defines the default model used inTurtleBot simulation to be the Burger model. You can also choose the Waffle model instead:

```
echo "export TURTLEBOT3_MODEL=burger" >> ~/.bashrc
```

9. Once these commands are executed (which wrote what's in the quotation marks into the `.bashrc` file), we need to source the `.bashrc` file for these things to take effect:

```
source ~/.bashrc
```

Now, the installation and basic setup for the TurtleBot3 simulation using ROS and Gazebo are complete.

## Starting the Simulation:

1. Launch your preferred Gazebo world based on your experimentation needs.

2. Run the SLAM (Simultaneous Localization and Mapping) node to create the map:

```
roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
```

3. Launch the teleoperation node again to enable driving the robot around the world and collecting data from its sensors to create a nearly complete and accurate map:

```
roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch. 
```
--------------------------------------------------------------------------------------------------------------------------------------------------\

# Task 3 
teachable machine 

1- open this website: https://teachablemachine.withgoogle.com/train/image

2- choose the number of classes that you want the machine to learn 

3- Upload Images to your classes *note that EACH class has to have similar images or images of the same kind*

4- train your model 

5- Upload a model image to start the comparison by the machine 

6- observe the results 
