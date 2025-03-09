cmake_minimum_required(VERSION 3.10)
project(DemoProject)

add_subdirectory(src)  # 构建 demolib 库
add_subdirectory(app)  # 构建可执行文件
