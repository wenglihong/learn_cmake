# 显示系统的HOME环境变量的值  
MESSAGE(STATUS $ENV{HOME})  
# 指定头文件查找目录  
# 注意，这里指定绝对路径。  
INCLUDE_DIRECTORIES($ENV{HOME}/coding/learn_cmake/HelloWorld/include)  
# 指定库文件查找目录（不能只指定头文件，也需要连接到库文件）  
# 注意，这里指定绝对路径, 也可通过设置系统环境变量LD_LIBRARY_PATH来指定。  
LINK_DIRECTORIES($ENV{HOME}/coding/learn_cmake/HelloWorld/lib ) 
# 生成可执行文件到项目的bin目录  
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)  
ADD_EXECUTABLE(main main.cpp)  
# 制定链接的外部Lib  
TARGET_LINK_LIBRARIES(main libhello.so)  

