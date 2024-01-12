cmake_minimum_required(VERSION 3.0.0)
project(raytracing CXX)

# Set to C++11
set ( CMAKE_CXX_STANDARD          17 )
set ( CMAKE_CXX_STANDARD_REQUIRED ON )
set ( CMAKE_CXX_EXTENSIONS        OFF )

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

set ( EXTERNAL
  src/external/stb_image.h
)

set ( RAYTRAYCING_SOURCE
    src/external/stb_image.h

    src/aabb.h
    src/camera.h
    src/color.h
    src/constant_medium.h
    src/hittable.h
    src/hittable_list.h
    src/interval.h
    src/material.h
    src/onb.h
    src/pdf.h
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

add_executable(raytracing       ${EXTERNAL} ${RAYTRAYCING_SOURCE})
add_executable(cos_cubed         src/cos_cubed.cc         )
add_executable(cos_density       src/cos_density.cc       )
add_executable(integrate_x_sq    src/integrate_x_sq.cc    )
add_executable(pi                src/pi.cc                )
add_executable(estimate_halfway  src/estimate_halfway.cc  )
add_executable(sphere_importance src/sphere_importance.cc )
add_executable(sphere_plot       src/sphere_plot.cc       )