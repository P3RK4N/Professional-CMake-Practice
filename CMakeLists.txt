cmake_minimum_required(VERSION 3.13)

#Non-Cache (Local) variable
set(BUILD_SHARED_LIBS OFF)

#Project initialisation
project(
   MyApp
   VERSION 0.1
   LANGUAGES C CXX
   )

#Libraries, console apps
add_subdirectory(src/MyExe)   #MyExe
add_subdirectory(src/MyLib)   #MyLib


#Linking
target_link_libraries(
   MyExe
   PRIVATE MyLib
   )

#Includes
get_target_property(loc MyLib location)
message(${loc})

target_include_directories(
   MyExe
   PRIVATE ${loc}
)

#Debug
message("Build Shared Libs: ${BUILD_SHARED_LIBS}")
message("Module paths: ${CMAKE_MODULE_PATH}")

set(COUNTER 0)

while(COUNTER LESS 10)
   message("Counter value is: ${COUNTER}")
   math(EXPR COUNTER "${COUNTER} + 1")
endwhile()