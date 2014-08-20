cmake_minimum_required(VERSION 2.8.3)
project(pein_msgs)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  actionlib_msgs
  geometry_msgs
  sensor_msgs
  std_msgs
  message_generation
)

## Generate messages in the 'msg' folder
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

## Generate services in the 'srv' folder
# add_service_files(
#   FILES
#   Service1.srv
#   Service2.srv
# )

## Generate actions in the 'action' folder
add_action_files(
  FILES
  Learn.action
  LearnObject.action
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  actionlib_msgs   geometry_msgs   sensor_msgs   std_msgs
)

###################################
## catkin specific configuration ##
###################################
## The catkin_package macro generates cmake config files for your package
## Declare things to be passed to dependent projects
## INCLUDE_DIRS: uncomment this if you package contains header files
## LIBRARIES: libraries you create in this project that dependent projects also need
## CATKIN_DEPENDS: catkin_packages dependent projects also need
## DEPENDS: system dependencies of this project that dependent projects also need
catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES pein_msgs
  CATKIN_DEPENDS actionlib_msgs geometry_msgs sensor_msgs std_msgs message_runtime
#  DEPENDS system_lib
)

###########
## Build ##
###########

## Specify additional locations of header files
## Your package locations should be listed before other locations
# include_directories(include)
include_directories(
  ${catkin_INCLUDE_DIRS}
)

## Declare a cpp library
# add_library(pein_msgs
#   src/${PROJECT_NAME}/pein_msgs.cpp
# )

## Declare a cpp executable
# add_executable(pein_msgs_node src/pein_msgs_node.cpp)

## Add cmake target dependencies of the executable/library
## as an example, message headers may need to be generated before nodes
#add_dependencies(Learn pein_msgs_generate_messages_cpp)
#add_dependencies(LearnObject pein_msgs_generate_messages_cpp)

## Specify libraries to link a library or executable target against
# target_link_libraries(pein_msgs_node
#   ${catkin_LIBRARIES}
# )
