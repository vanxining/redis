cmake_minimum_required(VERSION 3.2)

project(redis)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_STANDARD_REQUIRED TRUE)

include_directories(${CMAKE_CURRENT_LIST_DIR}/src)
include_directories(${CMAKE_CURRENT_LIST_DIR}/deps/hdr_histogram)
include_directories(${CMAKE_CURRENT_LIST_DIR}/deps/lua/src)

aux_source_directory(${CMAKE_CURRENT_LIST_DIR}/src _1)

add_executable(${PROJECT_NAME} ${_1})
