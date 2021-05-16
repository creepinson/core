cmake_minimum_required(VERSION 3.10)

# set the project name
project(ccore)

# add the source files
add_library(${PROJECT_NAME} src/color.h)

set_target_properties(${PROJECT_NAME} PROPERTIES LINKER_LANGUAGE CXX)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)
