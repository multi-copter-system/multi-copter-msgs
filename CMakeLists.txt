cmake_minimum_required(VERSION 3.0.2)
project(multi_copter_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
)

add_message_files(
  FILES
  Position.msg
)

add_service_files(
  FILES
  Command.srv
  Waypoint.srv
)

generate_messages(
    DEPENDENCIES
)

catkin_package(
  CATKIN_DEPENDS message_runtime
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)