cmake_minimum_required(VERSION 2.8.3)
project(rover_simulation)

find_package(catkin REQUIRED roslaunch)
catkin_package()

roslaunch_add_file_check(launch)

install(PROGRAMS
   nodes/ackermann_controller.py
   DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
install(DIRECTORY config
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
install(DIRECTORY launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
