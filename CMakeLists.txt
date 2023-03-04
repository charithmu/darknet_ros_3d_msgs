cmake_minimum_required(VERSION 3.5)

project(darknet_ros_3d_msgs)

# Set c++11 cmake flags
set(CMAKE_CXX_STANDARD 11)

find_package(catkin REQUIRED
  COMPONENTS
    actionlib_msgs
    geometry_msgs
    sensor_msgs
    std_msgs
    message_generation
)

add_message_files(
  FILES
    BoundingBox3d.msg
    BoundingBoxes3d.msg
)

generate_messages(
  DEPENDENCIES
    actionlib_msgs
    geometry_msgs
    sensor_msgs
    std_msgs
)

catkin_package(
  CATKIN_DEPENDS
    actionlib_msgs
    geometry_msgs
    sensor_msgs
    message_runtime
    std_msgs
)