cmake_minimum_required(VERSION 3.10)

# set the project name
project(ccore)

# Find source files
file(GLOB SOURCES src/*.cpp)
file(GLOB HEADERS src/*.h)

# add the source files
add_library(${PROJECT_NAME} ${HEADERS} ${SOURCES})
target_include_directories(${PROJECT_NAME} PUBLIC ${CMAKE_CURRENT_LIST_DIR}/include)

install(
    TARGETS ${PROJECT_NAME}
    LIBRARY DESTINATION ${CMAKE_INSTALL_LIBDIR}
    ARCHIVE DESTINATION ${CMAKE_INSTALL_LIBDIR}
    RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR}
    INCLUDES DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}
)


set_target_properties(${PROJECT_NAME} PROPERTIES LINKER_LANGUAGE CXX)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)
