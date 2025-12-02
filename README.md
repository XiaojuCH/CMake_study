# CMake_study
A repository to record my CMake study

## 使用流程

首先在项目目录创建一个CMakeLists.txt文件，注意这个文件名不要写错->   
    然后修改该文件内容   
完成后可新建一个bulid文件夹，以方便将管理新生成的项目文件->   
    进入build文件夹，终端输入```cmake ..```(这里的".."指的是CMakeLists.txt文件所在的目录，假设我们的build是根目录下的文件夹: 

    ```
    project/
    |—— main.cpp
    |—— CMakeLists.txt
    |
    |—— build
        |—— (我们所在的文件夹目录)  
    ```

    那么很显然CMakeLists.txt的相对位置就是..)   
输入该指令后会在build文件夹内生成若干文件->   
    我们再输入```make```指令即可得到所需的可执行文件->   
        之后再终端```./可执行文件名```即可运行

## CMakeLists.txt用法

cmake_minimum_required(VERSION 3.15) —— 指定用户使用CMake进行编译的最低版本为3.15   

project(test) —— 指定该项目的名称为test   

add_executable(app add.cpp div.cpp mult.cpp main.cpp sub.cpp) —— 定义工程会生成的可执行文件名字为app，然后这个app是由后面的源文件构成的

### set的用法


