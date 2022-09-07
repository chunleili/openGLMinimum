cmake_minimum_required(VERSION 3.20)
project(opengl)


#include path
include_directories(${PROJECT_SOURCE_DIR}/3rd/freeglut/include)

#link path
link_directories(${PROJECT_SOURCE_DIR}/3rd/freeglut/lib)


#set output dir of all target
set(OUT_DIR ${PROJECT_SOURCE_DIR}/bin)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${OUT_DIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${OUT_DIR})
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${OUT_DIR})
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY_DEBUG ${OUT_DIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_DEBUG ${OUT_DIR})
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY_DEBUG ${OUT_DIR})
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY_RELEASE ${OUT_DIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY_RELEASE ${OUT_DIR})
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY_RELEASE ${OUT_DIR})

#compile exe
add_executable(main main.cpp)

#link lib
target_link_directories(main PRIVATE ${PROJECT_SOURCE_DIR}/3rd/freeglut/lib/)
target_link_libraries(main PRIVATE freeglut_static.lib)