project(mytetra_dev)
cmake_minimum_required(VERSION 3.8.0)
add_definitions("-std=c++11")

message(CMake version = ${CMAKE_VERSION})

if(EXISTS ${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
    include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
    conan_basic_setup()
else()
    message(WARNING "The file conanbuildinfo.cmake doesn't exist, you have to run conan install first")
endif()




#add_subdirectory(app)
add_subdirectory(thirdParty/mimetex)