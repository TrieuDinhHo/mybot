## Indoor Delivery Robot Project
## Prerequisite Software
1. **Ubuntu 20.08**
2. **Ros2 Melodic**
3. Python 3.8 (or newer version)
## Prerequisite Hardware
1. STM32L432KC
2. Jetson Nano
3. Lidar(A1M8)
## How to run
1. **In Jetson Nano**
```c
cd mybot
```
```c
source install/setup.bash
```
```c
cd src 
```
```c
ros2 launch mybot launch_robot.launch.py
```
```c
ros2 launch mybot rplidar.launch.py 
```
2. **In Local Machine**
```c
cd mybot
```
```c
source install/setup.bash
```
```c
ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args -r /cmd_vel:=/diff_cont/cmd_vel_unstamped
```
```c
rviz2 -d src/mybot/config/slam_sim.rviz
```
```c
ros2 launch mybot navigation_launch.py use_sim_time:=false map_subcribe_transient_local:=true
```
## Demo Video
