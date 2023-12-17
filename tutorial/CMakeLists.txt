cmake_minimum_required(VERSION 3.12)
project(test)

find_package(Eigen3 REQUIRED)

set(SRC_DIR src)
set(SOURCES
    ${SRC_DIR}/main.cpp
)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

add_executable(test ${SOURCES})
target_include_directories(test PRIVATE ${EIGEN3_INCLUDE_DIRS})

