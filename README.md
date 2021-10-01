# Turtlebot3: Lab and Course Project

## Master Computer Setup (Laptop)
*Bootable Disk*
* Use ‘Part 2’ from this source to create the USB that contains a bootable version of Ubuntu 16.04
>https://www.wikihow.com/Dual-Boot-Windows-10-and-Ubuntu-16.04

*Disable UEFI Secure Boot*
* Follow the following link 
>https://itsfoss.com/disable-uefi-secure-boot-in-windows-8/ 
* If you are unable to change the setting from ‘enable’ to ‘disable’, you may need to create a supervisor password (Common with Acer laptops)
* Follow (https://itsfoss.com/disable-secure-boot-in-acer/) 
*Installing Ubuntu*
* Follow from Step: 3 in the link
https://itsfoss.com/install-ubuntu-1404-dual-boot-mode-windows-8-81-uefi/ 

**NOTE:**
* Partition should be (2 x The RAM of your computer) + 50Gb
* Only create the ‘root’ and ‘swap area’ area parts

## TurtleBot 3 Setup (Raspberry Pi 3)
```Ctrl+alt+t``` brings up terminal window

Use ```sudo``` in front of commands to act as administrator (especially when installing
programs)

The rest of the steps follow this manual starting from 6.2.1.1.
>http://emanual.robotis.com/docs/en/platform/turtlebot3/overview/

## Ubuntu Mate for Raspberry Pi
* Use fresh microSD card (Preferably 16Gb or more)
* Use the direct download link
* Right-click on the file and choose disk manager option to bring up window in the youtube
video
* Should only have ‘Free Space’ on the SD card
* Boot screen may have ‘Failed’ item, this is okay
* Wifi may not connect after installation, reboot and this should resolve itself.
* Update the system by typing ```sudo apt-get update``` and ```sudo apt-get upgrade``` in the terminal.
* Installation of ROS (check the website)

## OpenCR Firmware Upload (Check the website)
1.	Enter ```sudo raspi-config``` in a terminal window
2.	Select Interfacing Options
3.	Navigate to and select SSH
4.	Choose ```Yes```
5.	Select ```Ok```
6.	Choose ```Finish```

## Test Run
* [Laptop]
```
roscore
``` 
* [Raspberry Pi] 
```
roslaunch turtlebot3_bringup turtlebot3_robot.launch
```
* [Laptop] 
```
export TURTLEBOT3_MODEL=burger
roslaunch turtlebot3_bringup turtlebot3_remote.launch
rosrun rviz rviz -d ‘rospack find turtlebot3_description’ /rviz/demol.rviz
```
* [Laptop]
```
export TURTLEBOT3_MODEL=burger
roslaunch turtlebot_teleop turtlebot3 teleop key.launch
```
>Check the Turtlebot 3 online resource below: 
>http://emanual.robotis.com/docs/en/platform/turtlebot3/overview/
