cmake_minimum_required(VERSION 3.10)
project(cmake_static)
set(CMAKE_CXX_STANDARD 11)

set(LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/lib)
set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/bin)

include_directories(${CMAKE_SOURCE_DIR}/include)
link_directories(${CMAKE_SOURCE_DIR}/lib)

add_subdirectory(./src)


message("Generate main executable file")
add_executable(main main.cpp)

target_link_libraries(main
        hello_world
)
