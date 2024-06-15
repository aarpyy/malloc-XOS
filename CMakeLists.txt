cmake_minimum_required(VERSION 3.10)
project(lab5)

set(CMAKE_C_STANDARD 99)
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -g -DDRIVER -Wall -Wextra -Werror -O3 -Wno-unused-function -Wno-unused-parameter")

add_library(memlib memlib.c)
add_library(fcyc fcyc.c)
add_library(clock clock.c)
add_library(stree stree.c)
add_library(mman mman.c)

add_executable(mdriver mdriver.c mm.c)
target_link_libraries(mdriver memlib fcyc clock stree mman m)