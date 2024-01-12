#---------------------------------------------------------------------------------------------------
# CMake Build Configuration for the Ray Tracing Weekend Series
#
# See README.md for guidance.
#---------------------------------------------------------------------------------------------------

cmake_minimum_required ( VERSION 3.15.0)

project ( Raytracing2 LANGUAGES CXX )

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# Set to C++11
set ( CMAKE_CXX_STANDARD          11 )
set ( CMAKE_CXX_STANDARD_REQUIRED ON )
set ( CMAKE_CXX_EXTENSIONS        OFF )

# Source

set ( EXTERNAL
  src/external/stb_image.h
)

set ( SOURCE_RAYTRACING
  src/external/stb_image.h

  src/aabb.h
  src/bvh.h
  src/camera.h
  src/color.h
  src/constant_medium.h
  src/hittable.h
  src/hittable_list.h
  src/interval.h
  src/material.h
  src/perlin.h
  src/quad.h
  src/ray.h
  src/rtw_stb_image.h
  src/raytracing.h
  src/sphere.h
  src/texture.h
  src/vec3.h

  src/main.cc
)

add_executable(Raytracing2       ${EXTERNAL} ${SOURCE_RAYTRACING})
