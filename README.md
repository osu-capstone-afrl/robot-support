# MetaPackage for Robot Descriptions/Support Code

![Build Status: Github Actions - Melodic](https://github.com/osu-capstone-afrl/robot-support/actions/workflows/ci_Focal_Melodic.yml/badge.svg)

Includes copy of the motoman GP7 robot support package, end effector urdf's, and moveit configs.

## Packages Contained

| Package | Description |
| ------- | ----------- |
| motoman_gp7_support | Forked copy of ROS Industrial/Motoman support package. |
| motoman_gp7_moveit_config | MoveIt config for default Motoman GP7 robot. |
| nikon_d5600_support | End Effector Description w/ GP7 URDF connection options. |
| robot_gp7_d5600_moveit_config | MoveIt config building upon nikon_d5600_support package. |


## Documentation

Extensive documentation, usage notes, or general advice for this repo has been included in the repo Wiki.
<br>Access this wiki via the tabs above or this direct link: [osu-capstone-afrl/robot-support/wiki](https://github.com/osu-capstone-afrl/robot-support/wiki)

***

## Commonly Used Commands

Each of the below command sets gives..<br>
_Desired action, simulation, or screen_
```
$ Commands available for different robots or EEF configurations.
```

_View a Robot w/ TF Tree in RViz:_
```
roslaunch motoman_gp7_support test_gp7.launch
roslaunch nikon_d5600_support test_gp7_d5600.launch
```

_Connect to real robot to view ONLY live position of robot in RViz:_
```
roslaunch motoman_gp7_support robot_state_visualize_gp7.launch robot_ip:=192.168.1.31 controller:=yrc1000
```

_MoveIt: Simulate robot to test control and visuzlize in RViz:_
```
roslaunch motoman_gp7_moveit_config moveit_planning_execution.launch sim:=true
roslaunch robot_gp7_d5600_moveit_config moveit_planning_execution.launch sim:=true
```

_MoveIt: Connect to real robot to control and view live position of robot in RViz:_
```
roslaunch motoman_gp7_moveit_config moveit_planning_execution.launch sim:=false robot_ip:=192.168.1.31 controller:=yrc1000
roslaunch robot_gp7_d5600_moveit_config moveit_planning_execution.launch sim:=false robot_ip:=192.168.1.31 controller:=yrc1000
```


## Generic Instructions for Building ROS Workspace

Create your new project workspace..
<br>`mkdir -p ~/ws_project/src`

Clone this common set of packages into your project's local workspace/src..
<br>`git clone https://github.com/osu-capstone-afrl/robot-support.git ~/ws_project/src`

Remove the .GIT connection (optional)
_If not a developer, removing this will help ensure you don't accidentally push to this repo._
<br>`rm -rf ~/ws_project/src/.git`
