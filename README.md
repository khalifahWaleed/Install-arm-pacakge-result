# Install-arm-pacakge

# run this instruction inside your workspace:
$ rosdep install --from-paths src --ignore-src -r -y

# for noetic distro

$ sudo apt-get install ros-noetic-moveit
$ sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui
$ sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher
$ sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control

# Configuring Arduino with ROS
Install Arduino IDE in Ubuntu https://www.arduino.cc/en/software to install run 
$ sudo ./install.sh 
after unzipping the folder

# Install the arduino package and ros library
$ sudo apt-get install ros-indigo-rosserial-arduino
$ sudo apt-get install ros-indigo-rosserial

# Installing from Source onto the ROS workstation
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/
$ catkin_make
$ cd ~/catkin_ws/src
$ git clone https://github.com/smart-methods/arduino_robot_arm.git 
$ cd ~/catkin_ws

# Install ros_lib into the Arduino Environment
$ cd <sketchbook>/libraries
$ rm -rf ros_lib
$ rosrun rosserial_arduino make_libraries.py .

# Controlling the robot arm by joint_state_publisher
$ roslaunch robot_arm_pkg check_motors.launch



