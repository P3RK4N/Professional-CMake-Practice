cmake_minimum_required(VERSION 3.13)
include_guard()

add_executable(MyExe ${CMAKE_CURRENT_LIST_DIR}/main.cpp)

set_target_properties(MyExe PROPERTIES TARGET_LOCATION ${CMAKE_CURRENT_LIST_DIR})