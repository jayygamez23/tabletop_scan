project (tabletop_scan)
cmake_minimum_required(VERSION 2.8 FATAL_ERROR)

# set build type to release
set(CMAKE_BUILD_TYPE "Release")

# configure PCL
find_package(PCL 1.8.0 REQUIRED)
include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

# create create individual projects
add_executable (tabletop_scan tabletop_scan.cpp CloudVisualizer.cpp)
target_link_libraries(tabletop_scan ${PCL_LIBRARIES})


