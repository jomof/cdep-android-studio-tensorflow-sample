cmake_minimum_required(VERSION 3.4.1)

add_library( # Sets the name of the library.
             main

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             # Associated headers in the same location as their source
             # file are automatically included.
#             src/main/cpp/main.cpp
#             src/main/cpp/SDL_android_main.c
             src/main/cpp/frame_pair.cc
             src/main/cpp/image_neon.cc
             src/main/cpp/imageutils_jni.cc
             src/main/cpp/keypoint_detector.cc
             src/main/cpp/logging.cc
             src/main/cpp/object_detector.cc
             src/main/cpp/object_tracker.cc
             src/main/cpp/object_tracker_jni.cc
             src/main/cpp/optical_flow.cc
             src/main/cpp/rgb2yuv.cc
             src/main/cpp/time_log.cc
             src/main/cpp/tracked_object.cc
             src/main/cpp/utils_neon.cc
             src/main/cpp/yuv2rgb.cc
)

find_package(cdep-dependencies REQUIRED)
add_all_cdep_dependencies(main)

#target_link_libraries(main dl GLESv1_CM GLESv2 log android)

target_link_libraries(main log)
