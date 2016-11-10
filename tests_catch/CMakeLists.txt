cmake_minimum_required(VERSION 2.8.7)
project(Func CXX)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

include_directories(${CMAKE_CURRENT_SOURCE_DIR} /tests/)

add_library(Test STATIC ${CMAKE_CURRENT_SOURCE_DIR}/source/func.cpp ${CMAKE_CURRENT_SOURCE_DIR}/tests/main.cpp)

add_executable(tests ${CMAKE_CURRENT_SOURCE_DIR}/tests/func.cpp ${CMAKE_CURRENT_SOURCE_DIR}/tests/main.cpp)
