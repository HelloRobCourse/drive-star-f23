cmake_minimum_required(VERSION 3.11 FATAL_ERROR)
project(drive_star_checkpoint)

set(CMAKE_BUILD_TYPE RelWithDebInfo)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++14")

find_package(mbot_bridge REQUIRED)

# Drive star executable.
add_executable(drive_star
  src/drive_star.cpp
)
target_link_libraries(drive_star
  mbot_bridge_cpp
)
target_include_directories(drive_star PRIVATE
  include
)

if (CMAKE_BUILD_TYPE MATCHES Test)
endif()
