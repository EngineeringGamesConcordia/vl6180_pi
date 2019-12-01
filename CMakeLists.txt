cmake_minimum_required (VERSION 2.8.3)
project (VL6180X)

list(APPEND CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

find_package(libi2c-dev REQUIRED)
include_directories(AFTER ${I2CDEV_INCLUDE_DIRS})

add_library(VL6180X SHARED
    src/vl6180_pi.c
)

target_include_directories(VL6180X
    PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include
)


