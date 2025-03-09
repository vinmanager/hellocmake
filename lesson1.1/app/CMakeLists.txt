# 创建可执行文件
add_executable(demo_app main.cpp)

# 链接库并自动传递头文件路径
target_link_libraries(demo_app PRIVATE demolib::demolib)
