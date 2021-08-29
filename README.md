# Tiago TTS Package for SciRoc2EP1

This is a package containing all the required packages and dependencies of the Tiago tts package. The packages were gotten from two repositories, one is the **Pal Robotics** official Github pages ([Pal Robotics Tiago tutorial](https://github.com/pal-robotics/tiago_tutorials.git)) and a Tiago tts dependent package called _soundplay_ from **ROS Device Driver** GitHub page ([Audio Common](https://github.com/ros-drivers/audio_common.git)). The packages are put together in this repository merely for convenience reasons. For More information about this packages, visit their **ROS Wiki** at [sound_play](http://wiki.ros.org/sound_play) and [Pal Text to Speech](http://wiki.ros.org/Robots/TIAGo/Tutorials/TTS). Below is the instruction for compiling and launching the package successfully.

## How to Compile

- First, update the apt

```bash
apt update # sudo is not required for docker container
```

- Clone this repository into the _src_ folder of the workspace

```bash
git clone https://github.com/Omotoye/tiago_tts.git
```

- Initialize rosdep

```bash
rosdep init
rosdep update
```

- Use rosdep to get all the required dependencies of all the packages in the workspace

```bash
rosdep install --from-paths src --ignore-src -r -y
```

- run catkin build to build the packages.

```bash
catkin build
```

## How to Launch

You can try out some of the tutorials from the tiago_tutorial package.

The tutorial consists of two versions. The main version uses a GUI to allow the user to send strings for speech and visualize the feedback and result sent by the action server. To run this version launch the file without an extra argument

```bash
roslaunch tts tts.launch
```

The second version simply uses the terminal to display the same information and as input. To launch add the type argument

```bash
roslaunch tts tts.launch type:=terminal
```

Follow the prompt to send the action goal.

Refer to the wiki page for more information
