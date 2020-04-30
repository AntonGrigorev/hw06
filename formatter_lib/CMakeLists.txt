cmake_minimum_required(VERSION 3.4)
project(formatter)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(formatter STATIC ${CMAKE_CURRENT_SOURCE_DIR}/formatter.cpp)
include_directories(${CMAKE_CURRENT_SOURCE_DIR})
