## Requirments
### System packages
```
sudo apt install libdxflib-dev

```
## 新的ROS工作空间，我试了直接在原有工作空间上，但是编译一直出问题
```
export MRRP_DIR=$HOME/projects/catkin/tuw_multi_robot/
mkdir -p $MRRP_DIR/src
cd $MRRP_DIR/src
git clone https://github.com/tuw-robotics/tuw_multi_robot.git
git clone https://github.com/tuw-robotics/tuw_msgs.git
```
```
export ROS_VERSION=kinetic  # for Ubuntu 16.04

sudo apt install ros-$ROS_VERSION-map-server
sudo apt install ros-$ROS_VERSION-stage-ros
```
## 由于是在新建的工作空间，需要执行下面的命令再开始仿真
```
source ~/projects/catkin/tuw_multi_robot/devel/setup.sh
```
## 启动仿真
```
roslaunch tuw_multi_robot_demo demo.launch room:=cave  nr_of_robots:=3 
或者  
roslaunch tuw_multi_robot_demo demo.launch room:=cave cfg:=robot_2
```
