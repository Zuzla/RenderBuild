cmake_minimum_required(VERSION 3.0.0)
project(simpleraytracer CXX)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

add_executable(simpleraytracer simpleraytracer.cpp)
