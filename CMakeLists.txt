cmake_minimum_required(VERSION 2.8.4)
project(ffmpeg_streamer)

set(SOURCE_FILES1 ffmpeg_streamer.c)
set(SOURCE_FILES2 ffmpeg_receiver.c)

include_directories("/usr/local/include")

link_directories("/usr/local/lib")

add_executable(ffmpeg_streamer ${SOURCE_FILES1})
add_executable(ffmpeg_receiver ${SOURCE_FILES2})

target_link_libraries(ffmpeg_streamer "libavformat.a")

target_link_libraries(ffmpeg_streamer "libavutil.a")

target_link_libraries(ffmpeg_streamer "libavcodec.a")

target_link_libraries(ffmpeg_streamer "libavfilter.a")

target_link_libraries(ffmpeg_receiver "libavformat.a")

target_link_libraries(ffmpeg_receiver "libavutil.a")

target_link_libraries(ffmpeg_receiver "libavcodec.a")

target_link_libraries(ffmpeg_receiver "libavfilter.a")
