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

[![Demo CountPages alpha](https://share.gifyoutube.com/KzB6Gb.gif)](https://www.youtube.com/watch?v=ek1j272iAmc)


