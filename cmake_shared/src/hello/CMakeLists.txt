cmake_minimum_required(VERSION 3.10)
project(hello)
set(CMAKE_CXX_VERSION 11)

set(LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/lib)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin)

include_directories(${CMAKE_SOURCE_DIR}/include)
link_directories(${CMAKE_SOURCE_DIR}/lib)


message("Generate hello.so")
add_library(hello SHARED hello.cpp)