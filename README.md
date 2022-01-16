# Tb3GUILab
Tb3GUILab is a graphical interface used for controlling the Turtlebot 3. This interface has been developed over MATLAB using the [ROS Toolbox](https://es.mathworks.com/products/ros.html).

This GUI can be used directly after its download just by running <a href="https://github.com/albertozafra7/Tb3GUILab/blob/0fc50c6d0f1edbf9a2f4b65f916096fdbc6ff22c/Tb3Gui.mlapp">Tb3Gui.mlapp</a>.


## Prerequisites
<div>
  &#9744; <strong>Matlab</strong> (for its development it has been used the latest version of Matlab, 2021b).
</div>
<div>
  &#9744; <strong>Python 2.7 (recommended)</strong> or 3.X  depending on the Matlab installed version, python compatibility can be checked <a href="https://www.mathworks.com/content/dam/mathworks/mathworks-dot-com/support/sysreq/files/python-compatibility.pdf">here</a>.
  </div>
  <div>
  &#9744; <strong>ROS Toolbox for Matlab</strong>.
  </div>
  
Before using the software, please also check the requeriments of the ROS Toolbox, they can be found in the [link](https://es.mathworks.com/help/ros/gs/ros-system-requirements.html).

## Usage

After running the program the main window will ask the user the IP of the robot that is going to be connected to the graphical interface. That IP has to be introduced in the **ROS IP** field, as it is shown in the following image.

<p align="center"><img alt="Image" title="IP_Addres" src="/Pictures/IP_Address.PNG" /></p>

Once the user added the Ip Address, the "**disconnected**" button has to be pressed in order to connect to the remote robot. **Remember** if the robot it is not the Turtlebot 3, the line 462 has to be changed to "**turtleBotVersion = 2;**".
When the robot connects to the GUI the label of the disconnected button will change to "connected", the lamp will turn green and all the switches of the modes will become enable.

For disconnecting from the robot the user just needs to press the "connected" buton again. However, **if the robot gets disconnected while moving it will continue moving until endlessly**.

### Manual Mode

The *Manual Mode* allows the user to teleop the Turtlebot through a virtual "joystick" (It is just a set of state buttons), in order to ease the teleoperation process a lidar map and the robot camera are shown in the GUI window, as it is shown in the next video.

[![*Manual Mode*](/Pictures/Manual-Mode.gif)](https://drive.google.com/file/d/1BPtMOci_GTj1nfdoiA4JHb7sx_ISmwye/view?usp=sharing)


### Go To Mode

The *Go To Mode* is designed for performing a **simple navigation** in a previously mapped scenario, it uses the odometry in order to positionate the robot in the map. This map could be generated during the same execution of the program (by using the *Slam Mode*) or it could be loaded from a .mat, .pgm or .png file. However, those map files should be named as GeneratedMap.mat/.pgm/.png. The ideal use of this mode is to generate the map during the same execution. **This simple navigation usually does not works correctly**. Because it is still under development.

[![*Go To Mode*](/Pictures/Go-To-Mode.gif)](https://drive.google.com/file/d/1_f5_qK2bve0IPsm0CfGS9NCjdiXPSdCh/view?usp=sharing)

### Object Mode

The *Object Mode* implements an object follower example previously designed by [Mathworks](https://github.com/mathworks-robotics/getting-started-ros). It detects and follows a blue object. In addition the lineal and angular speed of the robot can be modified alongside to the distance between the robot and the object (Object Size) through the graphical interface.

[![*Object Mode*](/Pictures/Object-Mode.gif)](https://drive.google.com/file/d/1vv5-c2QiQbav-wcHykIYWO_iRp0chHo9/view?usp=sharing)

### Slam Mode

The *Slam Mode* was create in order to generate the map of the environment where the robot is. Its main purpose is to generate the map through the data received form the lidar scan. The map that is being created can be seen at the graphical window while using this mode, this process will be saved even though if the mode is changed. This mode also has implemented a "joystick" for the manual movement of the robot. However, the camera is not shown in this tab, so proceed carefully while controlling the robot. Finally, if the map is not correctly created the user can discard that map and generate another by pressing the "reset" button. On the other hand, if the map is correctly done and the user wants to save it it could be done by pressing the "save" button. Doing this the map will be saved as "GeneratedMap" in three different extensions (.mat, .pgm and .png).

[![*Slam Mode*](/Pictures/Slam-Mode.gif)](https://drive.google.com/file/d/1J4ZC-ucjJb-OSvKvcbgv6kjEAUk-S6qN/view?usp=sharing)

Enjoy the program <3
