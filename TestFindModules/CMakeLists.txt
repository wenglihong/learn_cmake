cmake_minimum_required(VERSION 2.8)
PROJECT(Test)
# CMAKE_MODULE_PATH定义必须放到前面
SET(CMAKE_MODULE_PATH $ENV{HOME}/coding/learn_cmake/CMakeModules)
#MESSAGE(STATUS $ENV{HOME}/workspace/CMakeModules)
ADD_SUBDIRECTORY(src)
