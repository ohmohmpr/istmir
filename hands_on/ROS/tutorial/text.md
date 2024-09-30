# 1 October 2024

## Goal

reimplement the Udacity here.

### How to run

```bash
docker compose up
```

### 1. Set up an environment in docker

1.1 Open Xhost, Seem like this command might give an security issue[MUST BE FIXED]
[ran GUI in docker](https://www.reddit.com/r/ROS/comments/s2qtkl/any_luck_running_gui_applications_through_ros2/)  
[Tutorial](https://wiki.ros.org/docker/Tutorials/GUI)  

Verify that they are working by using this command.

```bash
docker exec -it turtlesim_node bash
ros2 run turtlesim turtlesim_node

docker exec -it turtle_teleop_key bash &&
ros2 run turtlesim turtle_teleop_key

# the rqt
docker exec -it turtle_teleop_key bash &&
ros2 run turtlesim turtle_teleop_key

# the second turtle
docker exec -it turtle_teleop_key bash &&
ros2 run turtlesim turtle_teleop_key --ros-args --remap turtle1/cmd_vel:=turtle2/cmd_vel
```

[Turtlesim](https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools/Introducing-Turtlesim/Introducing-Turtlesim.html)  
[github interesting](https://github.com/ros/ros_tutorials/tree/humble/turtlesim)

### 2. Understanding nodes

Nodes should be responsible for a single, modular purpose(wheel motors).

The command ros2 run launches an executable from a package.  
<package_name> = turtlesim  
<executable_name> = turtlesim_node, turtle_teleop_key , draw_square, mimic  

### 2.1 Package and Executable

[WHAT IS PURPOSE of these two?]  
[Is node an Executable?] = I think so  

turtle_teleop_key , draw_square, mimic come from turtlesim/tutorials.  [Github code](https://github.com/ros/ros_tutorials/tree/humble/turtlesim/tutorials)  

### STOP HERE

[https://docs.ros.org/en/humble/Tutorials/Beginner-CLI-Tools/Understanding-ROS2-Nodes/Understanding-ROS2-Nodes.html#remapping]