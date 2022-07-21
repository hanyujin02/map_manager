# 3D Mapping For Autonomous Robots
This repo contains 3D [octomap](https://octomap.github.io/), [occupancy map](https://en.wikipedia.org/wiki/Occupancy_grid_mapping) and ESDF map for autonomous navigation.

### I. Install
```
sudo apt-get install ros-noetic-octomap*
git clone https://github.com/Zhefan-Xu/map_manager.git
cd ~/catkin_ws
catkin_make
```
### II. Run demo (simulatation)
Please intall package [uav_simulator](https://github.com/Zhefan-Xu/uav_simulator.git), then run the occupancy map launch: 
```
roslaunch uav_simulator start.launch
roslaunch map_manager occupancy_map.launch
roslaunch map_manager rviz.launch
```

or run ESDF map:
```
roslaunch uav_simulator start.launch
roslaunch map_manager esdf_map.launch
roslaunch map_manager rviz.launch
```

### III. Parameters
Please find parameters in ```map_manager/cfg/***.param``` files.

### IV. ROS Topics
Subsribe the following topics for occupancy and ESDF map:
  - Localization topic: ```robot/odometry``` or ```robot/pose``` (please enter the name of your topic in the parameter files)
  - Depth camera topic: ```camera/depth``` (defined in the config file)
Publish the following topics:
  - occupancy map visualization: ```occupancy_map/inflated_voxel_map```
  - esdf map visualization: ```esdf_map/inflated_voxel_map``` and ```esdf_map/esdf```

### V. C++ Code API
Example code:
```
```

