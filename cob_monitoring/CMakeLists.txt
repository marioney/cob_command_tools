cmake_minimum_required(VERSION 3.0.2)
project(cob_monitoring)

find_package(catkin REQUIRED COMPONENTS diagnostic_updater roscpp topic_tools)

catkin_package(
  CATKIN_DEPENDS roscpp topic_tools
)

include_directories(${catkin_INCLUDE_DIRS})



### Install ###
catkin_install_python(PROGRAMS
          src/cpu_monitor.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)


