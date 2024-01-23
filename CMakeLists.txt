cmake_minimum_required(VERSION 2.8.3)
project(rosaria_client)

## Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  geometry_msgs
  rosaria
)

###################################
## catkin specific configuration ##
###################################

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES turtle_test
#  CATKIN_DEPENDS roscpp rospy std_msgs
#  DEPENDS system_lib
)

###########
## Build ##
###########

## Specify additional locations of header files
include_directories(
  ${catkin_INCLUDE_DIRS}
)

## Declare a cpp executable
add_executable(go_three_second src/go_three_second.cpp)
add_executable(spin_counterclockwise src/spin_counterclockwise.cpp)
add_executable(spin_clockwise src/spin_clockwise.cpp)
add_executable(teleop src/teleop.cpp)
add_executable(print_state src/print_state.cpp)
add_executable(interface src/interface.cpp)
add_executable(enable_motors src/enable_motors.cpp)

## Add cmake target dependencies of the executable/library

## Specify libraries to link a library or executable target against
target_link_libraries(go_three_second 
  ${catkin_LIBRARIES}
)

target_link_libraries(spin_counterclockwise 
  ${catkin_LIBRARIES}
)

target_link_libraries(spin_clockwise 
  ${catkin_LIBRARIES}
)

target_link_libraries(teleop 
  ${catkin_LIBRARIES}
)

target_link_libraries(print_state
  ${catkin_LIBRARIES}
)

target_link_libraries(interface
  ${catkin_LIBRARIES}
)

target_link_libraries(enable_motors
  ${catkin_LIBRARIES}
)

