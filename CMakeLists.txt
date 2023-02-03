cmake_minimum_required(VERSION 3.2)

set(BUILD_SHARED_LIBS NO)

project(
   MyApp
   VERSION 0.1
   LANGUAGES C CXX
   )

add_library(MyLib src/MyLib/Utils.cpp)
add_executable(MyExe src/MyExe/main.cpp)

target_link_libraries(
   MyExe
   PRIVATE MyLib
   )