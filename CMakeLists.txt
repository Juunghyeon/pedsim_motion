cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

# Find Gazebo
find_package(gazebo REQUIRED)
include_directories(${GAZEBO_INCLUDE_DIRS})
link_directories(${GAZEBO_LIBRARY_DIRS})
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} ${GAZEBO_CXX_FLAGS}")

# Build our plugin
add_library(ActorPlugin SHARED src/ActorPlugin.cc)
target_link_libraries(ActorPlugin ${GAZEBO_LIBRARIES})

add_library(ActorPlugin_Walking_Sit SHARED src/ActorPlugin_Walking_Sit.cc)
target_link_libraries(ActorPlugin_Walking_Sit ${GAZEBO_LIBRARIES})

add_library(ActorPlugin_Walking SHARED src/ActorPlugin_Walking.cc)
target_link_libraries(ActorPlugin_Walking ${GAZEBO_LIBRARIES})

add_library(ActorPlugin_Running SHARED src/ActorPlugin_Running.cc)
target_link_libraries(ActorPlugin_Running ${GAZEBO_LIBRARIES})