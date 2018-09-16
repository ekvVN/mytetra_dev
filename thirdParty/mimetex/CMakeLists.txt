project(mimetex)
cmake_minimum_required(VERSION 3.8.0)

message(Touch mimeTeX qmake)


set(SOURCE_FILES
        mimetex.c
        gifsave.c)

set(HEADERS_FILES
        mimetex.h
        texfonts.h)

add_library(${PROJECT_NAME} ${SOURCE_FILES} ${HEADERS_FILES})
target_compile_definitions(${PROJECT_NAME} PUBLIC -DAA)


#OBJECTS_DIR = $${_PRO_FILE_PWD_}/build/obj
#DESTDIR = $${_PRO_FILE_PWD_}/build/bin
