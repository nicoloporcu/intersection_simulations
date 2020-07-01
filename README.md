# intersection_simulations

Simulates a gazebo intersection using turtlebot3.



### Install ros and create a ros catkin workspace:

Tutorial can be found at http://wiki.ros.org/ROS/Tutorials/InstallingandConfiguringROSEnvironment


### Install turtlebot3 model (In depth tutorials can be found at:)
https://emanual.robotis.com/docs/en/platform/turtlebot3/setup/#setup
https://emanual.robotis.com/docs/en/platform/turtlebot3/simulation/#ros-1-simulation 


First install the turtlebot3 dependencies 

```
sudo apt-get install ros-kinetic-joy ros-kinetic-teleop-twist-joy ros-kinetic-teleop-twist-keyboard ros-kinetic-laser-proc ros-kinetic-rgbd-launch ros-kinetic-depthimage-to-laserscan ros-kinetic-rosserial-arduino ros-kinetic-rosserial-python ros-kinetic-rosserial-server ros-kinetic-rosserial-client ros-kinetic-rosserial-msgs ros-kinetic-amcl ros-kinetic-map-server ros-kinetic-move-base ros-kinetic-urdf ros-kinetic-xacro ros-kinetic-compressed-image-transport ros-kinetic-rqt-image-view ros-kinetic-gmapping ros-kinetic-navigation ros-kinetic-interactive-markers
```

Clone turtlebot3 and the turtlebot3 simulations into the workspace 

```
 cd ~/(your workspace)/src/
 git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
 git clone -b kinetic-devel https://github.com/ROBOTIS-GIT/turtlebot3.git
 git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git
 cd ~/(your workspace) 
 catkin_make
```


### Clone catkin package for intersection simulation


Clone and run catkin make
```
 cd ~/(your workspace)/src/
 git clone https://github.com/nicoloporcu/intersection_simulations.git
 cd ~/(your workspace) 
 catkin_make
```


### Launching a turtlebot in a world

Export the turtlebot model (burger, waffle, or waffle pi) that you want to use. 
```
  export TURTLEBOT3_MODEL=burger
```
To make your choice permanent, add this line to your ``` ~/.bashrc ```

Then launch the turtlebot model in a world.
For example, to run a turtlebot on a stop intersection:
```
  roslaunch intersection_simulation intersection.launch
```
To launch three turtlebots in a stop intersection, run:
```
  roslaunch intersection_simulation intersection3turtlebot.launch
```

