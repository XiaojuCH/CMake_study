cmake_minimum_required(VERSION 3.15)
project(test1)

file(GLOB SRC ${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp)
set(EXECUTABLE_OUTPUT_PATH /home/xiaoju/Cmake_study/aa/bb/cc)
include_directories(${PROJECT_SOURCE_DIR}/include) # 设置头文件路径

# add_executable(app ${SRC})
set(LIBRARY_OUTPUT_PATH ~/cmake_study/CMake_study/V2/abcdefg) # 设置动/静态库保存目录
add_library(calc SHARED ${SRC})
