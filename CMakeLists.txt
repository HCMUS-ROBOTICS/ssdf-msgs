cmake_minimum_required(VERSION 3.0.2)
project(ssdf_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  geometry_msgs
  std_msgs
)

add_message_files(
  FILES
  Lane.msg
)

generate_messages(
  DEPENDENCIES
  geometry_msgs
  std_msgs
)

catkin_package(
 CATKIN_DEPENDS message_runtime geometry_msgs std_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)
