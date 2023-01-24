# Unitree ROS2

This is a Ros2 package designed to control the Unitree Go1 robot in low level mode. This repository was forked from 
[Unitree's 'Ros2 to Real'](https://github.com/unitreerobotics/unitree_ros2_to_real) package with some modifications to make adding custom low level control more streamlined. It also includes a copy of [unitree_legged_sdk v3.5.1](https://github.com/unitreerobotics/unitree_legged_sdk/releases/tag/v3.5.1).

Clone this repository in `unitree_ws/src`. If you want to be able to visualize the controls
in rviz as well (reccomended), clone my other package [go1_visualize](https://github.com/katie-hughes/go1_description)
into the same `unitree_ws/src` space.

## How to run
1. In `unitree_ws`, run `colcon build`. There is a warning about `BOOST_PRAGMA_MESSAGE` that I do not know how to resolve at the moment, but otherwise should build without error.
2. In another terminal, run `source install/setup.bash`
3. If you want to purely run the controls, run `ros2 launch unitree_legged_real low.launch.py`
4. If you want to run the controls plus the visualization in rviz, run `ros2 launch unitree_legged_real low_visualize.launch.py`

