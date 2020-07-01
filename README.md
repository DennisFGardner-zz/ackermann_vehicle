ackermann_vehicle
=================

ROS packages for simulating a vehicle with Ackermann steering

I forked this project from [@gkouros](https://github.com/gkouros/ackermann_vehicle). I modify to create a bare bones example of Ackermann steering with a large, truck-size, vehicle.

### Install
You may need to install additional packages to build. I needed: 

- `sudo apt install ros-melodic-ackermann-msgs`
- `sudo apt install ros-melodic-effort-controllers`

I build in `ackerman_ws`. You can replace this with the catkin workspace of your choice. 

- `mkdir -p ackerman_ws/src`
- `cd ackerman_ws/`
- `catkin build`
- `cd src/`
- `git clone https://github.com/DennisFGardner/ackermann_vehicle`
- `git clone https://github.com/gkouros/ackermann-drive-teleop`
- `cd ..`
- `catkin build`
- `source devel/setup.bash`

### Displaying, Launching, and Driving 

Display in RVIZ:

`roslaunch ackermann_vehicle_description ackermann_vehicle_rviz.launch`

Gazebo Simulation: 

`roslaunch ackermann_vehicle_gazebo ackermann_vehicle.launch`

Drive around with the keyboard: 

`rosrun ackermann_drive_teleop keyop.py 6.7 0.78 ackermann_vehicle/ackermann_cmd`