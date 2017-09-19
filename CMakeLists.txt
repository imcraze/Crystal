cmake_minimum_required(VERSION 3.3)
project(Crystal)

file(GLOB_RECURSE sources src/*.cpp src/*.h)
file(GLOB_RECURSE data res/*)

add_executable(Crystal ${sources} ${data})
target_compile_options(Crystal PUBLIC -std=c+11)
target_include_directories(Crystal PUBLIC src/)

file(COPY ${data} DESTINATION res)