cmake_minimum_required(VERSION 3.22.1)
PROJECT(screenCamera)

set(CMAKE_CXX_FLAGS "-std=c++11 -g -O2")

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include )

aux_source_directory(./src PROGRAM_SOURCE)
add_executable(screenCamera ${PROGRAM_SOURCE})

