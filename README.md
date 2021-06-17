# RoboND-Build my World
The "Build my world" project's purpose is to put into pratice the lessons learned as part of the RoboND Gazebo Basics lesson. 

Note: Both the workspace and the virtual machine were too slow to be able to work on any of them. I ended up installing ROS 2 Galactic (Ubuntu Focal) and Gazebo 9 under Ubuntu 20.04. I am aware there might be some compatibility issues and I will try to address them in due time.

### Directory Structure
```
    .myrobot                           # myrobot lab main folder 
    ├── model                          # Model files of a dummy model of a mobile robot with 
    │   ├── mymobilearm                # a manipulator.
    │   │   ├── model.config
    │   │   ├── model.sdf
    │   ├── mybuilding                 # Model files for an "approximation" of my flat...
    │   │   ├── model.config           # (nothing is up to scale)
    │   │   ├── model.sdf
    ├── script                         # Gazebo World plugin C++ script      
    │   ├── hello.cpp
    ├── world                          # Gazebo main (utopic) World containing the models.
    │   ├── myworld
    ├── CMakeLists.txt                 # Link libraries 
    └──                              
```
#### Add the library path to the Gazebo plugin path  

Prior to launching gazebo and loading "myworld".

```
export GAZEBO_PLUGIN_PATH=${GAZEBO_PLUGIN_PATH}:/home/aldo/UdacityRoboticsND/Project1BuildingMyWorld/build
```
