cmake_minimum_required(VERSION 3.10)
project(src)
set(CMAKE_CXX_STANDARD 11)

set(LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/lib)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin)

include_directories(${CMAKE_SOURCE_DIR}/include)
link_directories(${CMAKE_SOURCE_DIR}/lib)

add_subdirectory(hello)
add_subdirectory(world)


message("Generate hello_world.so")
add_library(hello_world SHARED hello_world.cpp)

target_link_libraries(hello_world
        hello
        world
)