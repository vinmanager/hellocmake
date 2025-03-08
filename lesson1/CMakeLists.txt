cmake_minimum_required(VERSION 3.10 FATAL_ERROR)
project(HelloCMake VERSION 1.0.0 LANGUAGES CXX)

# 收集源文件（推荐显式声明）
file(GLOB SRC_FILES 
    CONFIGURE_DEPENDS 
    src/*.cpp
)

# 生成可执行文件
add_executable(hello_main 
    ${SRC_FILES}
)

# 包含头文件路径（现代CMake推荐方式）
target_include_directories(hello_main 
    PRIVATE 
        ${PROJECT_SOURCE_DIR}/include  # 仅当前目标使用
)

# 设置C++标准
set_target_properties(hello_main PROPERTIES 
    CXX_STANDARD 17
    CXX_STANDARD_REQUIRED ON
)
