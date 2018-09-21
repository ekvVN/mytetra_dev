project(mytetra_dev)
cmake_minimum_required(VERSION 3.8.0)

message(CMake version = ${CMAKE_VERSION})

# Conan
if(EXISTS ${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
    include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
    conan_basic_setup()
else()
    message(WARNING "The file conanbuildinfo.cmake doesn't exist, you have to run conan install first")
endif()

# Qt
set(CMAKE_AUTOMOC ON)
set(CMAKE_AUTOUIC ON)
set(CMAKE_AUTORCC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)
find_package(Qt5 COMPONENTS
    Core
    Widgets
    Xml
    Svg
    Network
    PrintSupport
    REQUIRED)


add_subdirectory(tmp)
add_subdirectory(app)
add_subdirectory(thirdParty/mimetex)
