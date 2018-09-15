project(FoundationTimer)
cmake_minimum_required(VERSION 3.8.0)
add_definitions("-std=c++11")

message(CMake version = ${CMAKE_VERSION})
include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup(TARGETS)