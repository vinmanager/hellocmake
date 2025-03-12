# 定义数学库  
add_library(math_utils STATIC  
    src/matrix.cpp  
    src/vector.cpp  
)  

# 头文件路径（PUBLIC属性传递）  
target_include_directories(math_utils  
    PUBLIC  
        ${CMAKE_CURRENT_SOURCE_DIR}/include  # 使用者需包含  
    PRIVATE  
        ${CMAKE_CURRENT_SOURCE_DIR}/src      # 仅内部使用  
)  

# 读取父目录变量  
if(ENABLE_DEBUG)  
    target_compile_options(math_utils PRIVATE -g3)  
endif()  

# 向上传递变量  
set(MATH_LIB_READY TRUE PARENT_SCOPE)  
