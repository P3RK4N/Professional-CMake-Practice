cmake_minimum_required(VERSION 3.13)
include_guard()

add_library(MyLib ${CMAKE_CURRENT_LIST_DIR}/Utils.cpp)

set_target_properties(MyLib PROPERTIES location ${CMAKE_CURRENT_LIST_DIR})