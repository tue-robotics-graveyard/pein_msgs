cmake_minimum_required(VERSION 2.8.3)
project(pein_msgs)

find_package(catkin REQUIRED COMPONENTS
  actionlib_msgs
  geometry_msgs
  sensor_msgs
  std_msgs
  message_generation
)

add_message_files(
  FILES
  FaceArray.msg
  Face.msg
  Hypothesis.msg
  ModuleStatus.msg
  ObjectImage.msg
  ODM.msg
  ROI.msg
  Segmentation.msg
  Segment.msg
)

add_action_files(
  FILES
  Learn.action
  LearnObject.action
)

generate_messages(
  DEPENDENCIES
  actionlib_msgs   geometry_msgs   sensor_msgs   std_msgs
)

###################################
## catkin specific configuration ##
###################################
catkin_package(
  CATKIN_DEPENDS
    actionlib_msgs
    geometry_msgs
    sensor_msgs
    std_msgs
    message_runtime
)
