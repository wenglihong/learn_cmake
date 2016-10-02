# 添加头文件的查找目录  
INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/include)  
## 生成各种目标(target)文件: 可执行文件、动态库、静态库  
# 指定可执行文件的输出目录，输出到bin下面  
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)  
# 指定可执行文件名(hello)和相关源文件   
ADD_EXECUTABLE(hello test.cpp Hello.cpp)  
# 指定库文件输出路径  
SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)  
# 生成动态库  
# 注意，前面已经使用target文件名hello，这里不能再用。  
ADD_LIBRARY(hello_so SHARED Hello.cpp)  
# 设置库输出名为 hello => libhello.so  
SET_TARGET_PROPERTIES(hello_so PROPERTIES OUTPUT_NAME "hello")  
# 生成静态库  
# 注意，前面已经使用target文件名hello，这里不能再用。  
ADD_LIBRARY(hello_a STATIC Hello.cpp)  
# 设置输库出名为 hello => libhello.a  
SET_TARGET_PROPERTIES(hello_a PROPERTIES OUTPUT_NAME "hello")  
