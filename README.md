# swri_console

| master | dashing-devel |
| ------ | ------------- |
| [![Build Status](https://travis-ci.org/swri-robotics/swri_console.svg?branch=master)](https://travis-ci.org/swri-robotics/swri_console) | [![Build Status](https://travis-ci.org/swri-robotics/swri_console.svg?branch=dashing-devel)](https://travis-ci.org/swri-robotics/swri_console) |

![screenshot](doc/images/screenshot.png)

swri_console is an alternative to rqt_console for viewing the ROS console output.  swri_console was written to scale well to large systems with heavy console output.  It stays responsive under fire and allows users to quickly find information to track down problems.

### Installation

The `master` branch compiles and runs on ROS Kinetic and Melodic; the `dashing-devel` branch compiles and runs on ROS 2 Dashing and Eloquent.

To install a binary release:

```bash
sudo apt install ros-${ROSDISTRO}-swri-console
```

### Usage

ROS 1:

```
rosrun swri_console swri_console
```

ROS 2:

```
ros2 run swri_console swri_console
```

### Features

- High performance; swri_console handles receiving thousands of logs per second and storing millions in memory while staying responsive
- Ctrl or shift-click to quickly select which nodes you want to monitor
- Hide or show log messages based on substring matches, or, if you need more power, regular expressions
- Hide, show, and colorize log messages based on severity
- Save and load log messages to text files
- Save and load log messages directly from the `/rosout` topic in a bag file
   - *Not supported in ROS 2 yet*
- Right-click on nodes to dynamically set their logger levels
   - *Not supported in ROS 2 yet*
