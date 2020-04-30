cmake_minimum_required(VERSION 3.4)
project(solver)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib ${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib ${CMAKE_CURRENT_BINARY_DIR}/sub3)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib ${CMAKE_CURRENT_BINARY_DIR}/sub4)

add_executable(solver ${CMAKE_CURRENT_SOURCE_DIR}/equation.cpp)
target_link_libraries(solver formatter_ex solver_lib)
