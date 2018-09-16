project(HelloQt)
cmake_minimum_required(VERSION 3.8.0)

add_executable(${PROJECT_NAME} WIN32
        mainwindow.ui
        mainwindow.cpp
        mainwindow.h
        main.cpp)
target_link_libraries(${PROJECT_NAME} Qt5::Widgets)