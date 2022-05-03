# hector_slam_lms11
Hector slam on sick safety scanner lms11
Terminal 1:
LAUNCH THE LMS11 SENSOR NODE 

user:~/test_ws/source /opt/ros/melodic.setup.bash
user:~/test_ws/catkin build or catkin_make
user:~/test_ws/source ./devel/setup.bash
user:~/test_ws/roslaunch slam_test lms11.launch 

Terminal 2:
LAUNCH THE HECTOR SLAM NODE 

user:~/test_ws/source /opt/ros/melodic.setup.bash
user:~/test_ws/catkin build or catkin_make
user:~/test_ws/source ./devel/setup.bash
user:~/test_ws/roslaunch slam_test hector_map.launch 

Terminal 3:
OPEN RVIZ AND ADD map,laser scan to view the map 

user:~/test_ws/source /opt/ros/melodic.setup.bash
user:~/test_ws/catkin build or catkin_make
user:~/test_ws/source ./devel/setup.bash
user:~/test_ws/rosrun rviz rviz

Links to follow 
https://github.com/tu-darmstadt-ros-pkg/hector_slam
http://wiki.ros.org/LMS1xx
https://github.com/clearpathrobotics/LMS1xx/tree/melodic-devel
add everything as submodule and make a change on it
sudo apt-get install ros-melodic-hector-slam
sudo apt-get install ros-melodic-lms1xx

In launch file you need to use your sensor id as host
<arg name="host" default="192.168.1.14" />  it is default
<arg name="host" default="192.168.12.138" />  it is my id 
Use soaps software to get your Id 
https://github.com/SICKAG/sick_scan/blob/master/doc/ipconfig/ipconfig.md
