project(note08)
cmake_minimum_required(VERSION 2.8)
aux_source_directory(. SRC_LIST)
add_executable(${PROJECT_NAME} ${SRC_LIST})


#CMake find SDL
#https://cmake.org/cmake/help/v3.5/module/FindSDL.html
find_library(MACOS_COCOA cocoa)
if (NOT MACOS_COCOA)
    message(FATAL_ERROR "<err> need cocoa framework")
endif()

target_link_libraries(note08 avcodec avformat avutil swscale swresample SDLmain SDL ${MACOS_COCOA})
