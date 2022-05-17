cmake_minimum_required(VERSION 3.10)

# set the project name
project(SimpleGameEngine)

# include_directories(${CMAKE_SOURCE_DIR}/inc)
# link_directories(${CMAKE_SOURCE_DIR}/lib)

# set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
# set(SOURCE_FILES ${CMAKE_CURRENT_SOURCE_DIR}/PhysicsEngineCyclone)
# set(SOURCE_FILES PhysicsEngineCyclone)
# add_library(cyclone STATIC ${SOURCE_FILES})
add_subdirectory(PhysicsEngineCyclone)