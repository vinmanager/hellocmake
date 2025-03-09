# 创建库目标
add_library(demolib SHARED demo.cpp)

# 添加头文件路径（PUBLIC 表示库自身和依赖它的目标都能使用）
target_include_directories(demolib
  PUBLIC 
    ${PROJECT_SOURCE_DIR}/include  # 使得 #include <demolib/demo.hpp> 有效
)

# 可选：生成一个命名空间目标（如 demolib::demolib）
add_library(demolib::demolib ALIAS demolib)
