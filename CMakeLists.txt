project(FoundationTimer)
cmake_minimum_required(VERSION 3.12.1)
add_definitions("-std=c++11")

message(${CMAKE_BINARY_DIR})
include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup(TARGETS)