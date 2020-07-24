cmake_minimum_required(VERSION 3.16)
project(tinyosc VERSION 0.1.0)

set(CMAKE_C_STANDARD 99)

add_library(tinyosc STATIC tinyosc.c tinyosc.h)
target_include_directories(tinyosc PUBLIC ${CMAKE_CURRENT_LIST_DIR})

add_executable(example main.c)
target_link_libraries(example tinyosc)
