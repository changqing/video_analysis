cmake_minimum_required(VERSION 3.5)
project(tamper)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
#require OpenCV
FIND_PACKAGE( OpenCV 3.0.0 REQUIRED )
MESSAGE("OpenCV version : ${OpenCV_VERSION}")
include_directories(${OpenCV_INCLUDE_DIRS})
link_directories(${OpenCV_LIB_DIR})

set(SOURCE_FILES main.cpp)
add_executable(tamper ${SOURCE_FILES})
TARGET_LINK_LIBRARIES(tamper ${OpenCV_LIBS})