cmake_minimum_required(VERSION 3.0)
project("Excute" CXX C)

set(INC_DIR inc)
set(SRC_DIR src)
set(DOC_DIR doc)
set(SCRIPT_DIR script)
set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_FLAGS "-std=c++11")
set(CMAKE_C_FLAGS "-std=gnu99")
# 没用，改不了编译器
set(CMAKE_C_COMPILER D:/GreenApp/mingw64/bin/x86_64-w64-mingw32-gcc.exe)

include_directories(${INC_DIR})

add_compile_options(-Wall)
add_subdirectory(${SRC_DIR} bin)
add_subdirectory(${DOC_DIR})
add_subdirectory(${SCRIPT_DIR})

message(STATUS "编译器【C】: ${CMAKE_C_COMPILER}")
message(STATUS "编译器【C++】: ${CMAKE_CXX_COMPILER}")
message(STATUS "编译器参数【C】: ${CMAKE_C_FLAGS}")
message(STATUS "编译器参数【C++】:${CMAKE_CXX_FLAGS}")
message(STATUS "工程类型: ${CMAKE_BUILD_TYPE}")
message(STATUS "二进制文件位置: ${CMAKE_BINARY_DIR}")
message(STATUS "二进制文件位置: ${PROJECT_BINARY_DIR}")
message(STATUS "二进制文件位置: ${CMakeIntroduction_BINARY_DIR}")
message(STATUS "源代码位置: ${CMAKE_SOURCE_DIR}")
message(STATUS "源代码位置: ${PROJECT_SOURCE_DIR}")
message(STATUS "源代码位置: ${CMakeIntroduction_SOURCE_DIR}")
message(STATUS "可执行文件的输出目录: ${EXECUTABLE_OUTPUT_PATH}")
message(STATUS "库输出目录: ${LIBRARY_OUTPUT_PATH}")
message(STATUS "头文件目录: ${CMAKE_INCLUDE_PATH}")