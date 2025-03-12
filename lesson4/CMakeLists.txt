cmake_minimum_required(VERSION 3.12)  
project(Autopilot LANGUAGES CXX)  

# 添加子模块  
add_subdirectory(lib/math)  
add_subdirectory(src)  
add_subdirectory(tests EXCLUDE_FROM_ALL)  # 测试模块默认不构建  

# 全局变量传递示例  
set(ENABLE_DEBUG ON)  
message("全局变量传递测试: ${ENABLE_DEBUG}")  
