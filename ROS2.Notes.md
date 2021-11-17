## Soucre ROS2
$ . ~/ros2_foxy/ros2-linux/setup.bash #Local installation
$ source /opt/ros/foxy/setup.bash #Global

## ROS2 Create Workspace
$ mkdir -p ~/dev_ws/src
$ cd ~/dev_ws/src

#In the dev_ws/src directory, clone a repo

$ rosdep install -i --from-path src --rosdistro foxy -y

## Install colcon for ros2
$ sudo sh -c 'echo "deb [arch=amd64,arm64] http://repo.ros2.org/ubuntu/main `lsb_release -cs` main" > /etc/apt/sources.list.d/ros2-latest.list'
$ curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

$ sudo apt update
$ sudo apt install python3-colcon-common-extensions

## For agv-evobot-ros2-joy installation
sudo apt-get install libssl-dev

colcon build
