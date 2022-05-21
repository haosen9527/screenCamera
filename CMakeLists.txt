cmake_minimum_required(VERSION 3.22.1)
PROJECT(screenCamera)

set(CMAKE_CXX_FLAGS "-std=c++11 -g -O2")

find_package(OpenCV REQUIRED)

message(STATUS "    OpenCV library status:")
message(STATUS "    version: ${OpenCV_VERSION}")
#message(STATUS "    libraries: ${OpenCV_LIBS}")
message(STATUS "    include path: ${OpenCV_INCLUDE_DIRS}")

include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}/include
    ${OpenCV_INCLUDE_DIRS} 
    )

link_directories(
    ${OpenCV_LIBS}
)


aux_source_directory(./src PROGRAM_SOURCE)
add_executable(screenCamera ${PROGRAM_SOURCE})

target_link_libraries(screenCamera
${OpenCV_LIBS}
)

