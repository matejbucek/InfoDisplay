cmake_minimum_required(VERSION 3.22.1)
project(infodisplay)

SET(CMAKE_SYSTEM_NAME Linux)
SET(CMAKE_SYSTEM_VERSION 1)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_COMPILER clang++)
#set(CMAKE_CXX_COMPILER arm-linux-gnueabihf-g++)
#SET(CMAKE_C_COMPILER arm-linux-gnueabihf-gcc)

#SET(CMAKE_FIND_ROOT_PATH ./toolchain/tools/arm-bcm2708/arm-rpi-4.9.3-linux-gnueabihf/arm-linux-gnueabihf/sysroot/)

#SET(CMAKE_FIND_ROOT_PATH_MODE_PROGRAM NEVER)
#SET(CMAKE_FIND_ROOT_PATH_MODE_LIBRARY ONLY)
#SET(CMAKE_FIND_ROOT_PATH_MODE_INCLUDE ONLY)

set(SOURCES
        src/main.cpp
        )

find_package(raylib 3.0 REQUIRED) # Requires at least version 3.0


    #add_subdirectory(lib)
    #include_directories(lib)

add_executable(infodisplay ${SOURCES})
target_link_libraries(${PROJECT_NAME} raylib)
#target_link_libraries( app-templates LibOptions )
