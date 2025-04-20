cmake_minimum_required(VERSION 3.10)
project(facedetection)

# Find OpenCV
find_package(OpenCV REQUIRED)

# Include OpenCV directories
include_directories(${OpenCV_INCLUDE_DIRS})

# Add source files
add_executable(facedetection main.cpp)

# Link OpenCV libraries
target_link_libraries(facedetection ${OpenCV_LIBS})
