if(0)
# 这里是最传统的办法
    cmake_minimum_required(VERSION 3.15)
    project(test)
    set(SRC add.cpp div.cpp mult.cpp main.cpp sub.cpp) # 这里将后面的源文件保存到变量SRC里面了
    set(EXECUTABLE_OUTPUT_PATH /home/xiaoju/Cmake_study/build) # 这里可以设置生成的可执行文件的路径
    set(CMAKE_CXX_STANDARD 17) # 这里是设置使用的C++版本特性
    add_executable(app add.cpp div.cpp mult.cpp main.cpp sub.cpp)
    # add_executable(app ${SRC}) # 这句的功能跟上句相同
endif()

if(0)
# 这是没有嵌套目录 比如说/include跟/src 的情况
    cmake_minimum_required(VERSION 3.15)
    project(test)
    # aux_source_directory(${PROJECT_SOURCE_DIR} SRC) # 这里是自动搜索代码
    file(GLOB SRC ${CMAKE_CURRENT_SOURCE_DIR} /*.cpp) # 同理
    set(EXECUTABLE_OUTPUT_PATH /home/xiaoju/Cmake_study/aa/bb/cc) # 这里可以设置生成的可执行文件的路径

    add_executable(app ${SRC})
endif()



cmake_minimum_required(VERSION 3.15)
project(test)

file(GLOB SRC ${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp)
set(EXECUTABLE_OUTPUT_PATH /home/xiaoju/Cmake_study/aa/bb/cc)
include_directories(${PROJECT_SOURCE_DIR}/include) # 设置头文件路径

add_executable(app ${SRC})
