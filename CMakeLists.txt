cmake_minimum_required(VERSION 2.8.3)
project(camera_scene_classifier)

## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED message_generation std_msgs)

## Generate messages in the 'msg' folder
add_message_files(
  FILES
  SceneClassification.msg
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime roscpp std_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

install()
