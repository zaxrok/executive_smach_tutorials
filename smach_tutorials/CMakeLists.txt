cmake_minimum_required(VERSION 2.8.3)
project(smach_tutorials)

find_package(catkin REQUIRED COMPONENTS
  genmsg
  actionlib_msgs
  actionlib
  geometry_msgs
)

catkin_python_setup()

add_action_files(
  DIRECTORY
  action
  FILES
  Test.action
)

generate_messages(
  DEPENDENCIES
  geometry_msgs
  actionlib_msgs
)