project(note01)
cmake_minimum_required(VERSION 2.8)
aux_source_directory(. SRC_LIST)
add_executable(${PROJECT_NAME} ${SRC_LIST})

# link ffmpeg library , libavcodec, libavformat
link_directories(/usr/local/Cellar/ffmpeg/3.0.2/lib)
target_link_libraries(note01 avcodec avformat avutil swscale)
