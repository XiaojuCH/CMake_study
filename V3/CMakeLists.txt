cmake_minimum_required(VERSION 3.15)
project(test1)

file(GLOB SRC ${CMAKE_CURRENT_SOURCE_DIR}/*.cpp)
include_directories(${PROJECT_SOURCE_DIR}/include) # 设置头文件路径

link_libraries(calc) # 这里是加库文件

link_directories(${CMAKE_CURRENT_SOURCE_DIR}/lib1) 
# 这里的是去指定一个我们自定义的库文件(因为上面的link_libraries
#指令只能加载系统的库)

add_executable(app ${SRC})
