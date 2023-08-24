<img width="960" alt="Screenshot 2023-06-25 230240" src="https://github.com/adijams01/my_bot/assets/92617405/8a4ac906-209a-4cf9-9070-852704c5f9a6">

## Working on 
* ROS2 version : foxy/humble/galactic
* Ubuntu 20.04/22.04
* virtual Machine

## Issues
* ros2_control problem with humble
* odometry issues with foxy
#### Worked Fine with galactic (not on V.M.)

## Regular Commands
```
colcon build --symlink-install
```
```
source install/setup.bash
```
```
source /opt/ros/foxy/setup.bash
```
```
ros2 launch my_bot rsp.launch.py
```
```
rviz2
```
```
ros2 run joint_state_publisher_gui joint_state_publisher_gui
```
```
ros2 launch my_bot launch_sim.launch.py
```
```
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```
```
ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r /cmd_vel:=/diff_cont/cmd_vel_unstamped
```
```
ros2 launch slam_toolbox online_async_launch.py params_file:=./my_bot/config/mapper_params_online_async.yaml use_sim_time:=true
```
```
ros2 launch nav2_bringup navigation_launch.py use_sim_time:=true
```
```
ros2 run twist_mux twist_mux --ros-args --params-file ./my_bot/config/twist_mux.yaml
```
```
ros2 run nav2_map_server map_server --ros-args -p yaml_filename:=my_map_save.yaml -p use_sim_time:=true
```
```
ros2 run nav2_util lifecycle_bringup map_server
```
```
ros2 run nav2_util lifecycle_bringup amcl
```
```
ros2 run nav2 amcl amcl --ros-args -p use_sim_time:=true
```
```
killall gzserver
```
```
killall gzclient
```
