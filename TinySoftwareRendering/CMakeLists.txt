cmake_minimum_required(VERSION 3.0.0)
project(TinySoftwareRendering VERSION 0.1.0 LANGUAGES C CXX)
set (CMAKE_CXX_STANDARD 17)

add_executable(TinySoftwareRendering 
    src/main.cpp
    src/geometry.cpp
    src/geometry.h
    src/gl.cpp
    src/gl.h
    src/model.cpp
    src/model.h
    src/tgaimage.cpp
    src/tgaimage.h
)

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
