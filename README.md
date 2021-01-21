# Default ROS Workspace

Default workspace for the OSU Capstone team. Includes motoman GP7 robot support package and moveit_config.

## Suggested Usage

Utilize this metapackage set as a starting point for ROS implementations of code. The goal of this repository is to contain all robot and vision support packages needed for the project. Additionally, common end-effector support packages will be included.


### How To Use

Create your new project workspace..
<br>`mkdir -p ~/ws_project/src`

Clone this common set of packages into your project's local workspace/src..
<br>`git clone https://github.com/osu-capstone-afrl/ws_basic.git ~/ws_project/src`

Remove the .GIT connection
<br>`rm -rf ~/ws_project/src/.git`
