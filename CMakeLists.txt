cmake_minimum_required(VERSION 3.10)
project(FootMeasurement)

find_package(OpenCV REQUIRED)

set(OpenCV_LIBRARIES_DIRS "${OpenCV_INCLUDE_DIRS}/../x64/vc15/lib")
message(STATUS "Using opencv ${OpenCV_VERSION}")
message(STATUS "Using OpenCV_INCLUDE_DIRS ${OpenCV_INCLUDE_DIRS}")
message(STATUS "Using OpenCV_LIBRARIES_DIRS ${OpenCV_LIBRARIES_DIRS}")
message(STATUS "Using OpenCV_LIBS ${OpenCV_LIBS}")

include_directories(${OpenCV_INCLUDE_DIRS})
link_directories(${OpenCV_LIBRARIES_DIRS})

SET(CMAKE_BUILD_TYPE "Release")

ADD_EXECUTABLE(FootMeasurement Measurement.cpp )
target_link_libraries(FootMeasurement opencv_world453.lib)
