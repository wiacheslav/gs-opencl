cmake_minimum_required(VERSION 3.20)
project(ocl_gs)

set(CMAKE_CXX_STANDARD 17)

find_package(OpenCL REQUIRED)

add_executable(ocl_gs main.cpp)
add_executable(device_details device_details.cpp)

target_link_libraries(ocl_gs OpenCL::OpenCL)
target_link_libraries(device_details OpenCL::OpenCL)