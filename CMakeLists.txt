cmake_minimum_required(VERSION 3.4)

# project name
project(ProjectName)

# set version number
set (MAJOR 1)
set (MINOR 0)

set(CMAKE_BINARY_DIR ${CMAKE_CURRENT_SOURCE_DIR}/target)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

add_subdirectory(src/math)

set(SOURCE_FILES
        src/main.cpp)

add_executable(ProjectName ${SOURCE_FILES})

target_link_libraries(ProjectName shared)