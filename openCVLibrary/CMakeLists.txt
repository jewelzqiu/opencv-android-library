# For more information about using CMake with Android Studio, read the
# documentation: https://d.android.com/studio/projects/add-native-code.html

# Sets the minimum version of CMake required to build the native library.

cmake_minimum_required(VERSION 3.4.1)

set(CMAKE_VERBOSE_MAKEFILE on)
set(libs "${CMAKE_SOURCE_DIR}/src/main/jniLibs")
include_directories(${CMAKE_SOURCE_DIR}/src/main/cpp/include)

add_library(libopencv_saliency SHARED IMPORTED )
set_target_properties(libopencv_saliency PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_saliency.a")

add_library(libopencv_photo SHARED IMPORTED )
set_target_properties(libopencv_photo PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_photo.a")

add_library(libopencv_bgsegm SHARED IMPORTED )
set_target_properties(libopencv_bgsegm PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_bgsegm.a")

add_library(libopencv_videoio SHARED IMPORTED )
set_target_properties(libopencv_videoio PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_videoio.a")

add_library(libopencv_surface_matching SHARED IMPORTED )
set_target_properties(libopencv_surface_matching PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_surface_matching.a")

add_library(libopencv_datasets SHARED IMPORTED )
set_target_properties(libopencv_datasets PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_datasets.a")

add_library(libopencv_calib3d SHARED IMPORTED )
set_target_properties(libopencv_calib3d PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_calib3d.a")

add_library(libopencv_xphoto SHARED IMPORTED )
set_target_properties(libopencv_xphoto PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_xphoto.a")

add_library(libopencv_features2d SHARED IMPORTED )
set_target_properties(libopencv_features2d PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_features2d.a")

add_library(libopencv_img_hash SHARED IMPORTED )
set_target_properties(libopencv_img_hash PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_img_hash.a")

add_library(libopencv_dnn SHARED IMPORTED )
set_target_properties(libopencv_dnn PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_dnn.a")

add_library(libopencv_core SHARED IMPORTED )
set_target_properties(libopencv_core PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_core.a")

add_library(libopencv_rgbd SHARED IMPORTED )
set_target_properties(libopencv_rgbd PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_rgbd.a")

add_library(libopencv_plot SHARED IMPORTED )
set_target_properties(libopencv_plot PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_plot.a")

add_library(libopencv_java3 SHARED IMPORTED )
set_target_properties(libopencv_java3 PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_java3.so")

add_library(libopencv_imgcodecs SHARED IMPORTED )
set_target_properties(libopencv_imgcodecs PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_imgcodecs.a")

add_library(libopencv_highgui SHARED IMPORTED )
set_target_properties(libopencv_highgui PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_highgui.a")

add_library(libopencv_fuzzy SHARED IMPORTED )
set_target_properties(libopencv_fuzzy PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_fuzzy.a")

add_library(libopencv_structured_light SHARED IMPORTED )
set_target_properties(libopencv_structured_light PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_structured_light.a")

add_library(libopencv_video SHARED IMPORTED )
set_target_properties(libopencv_video PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_video.a")

add_library(libopencv_tracking SHARED IMPORTED )
set_target_properties(libopencv_tracking PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_tracking.a")

add_library(libopencv_superres SHARED IMPORTED )
set_target_properties(libopencv_superres PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_superres.a")

add_library(libopencv_reg SHARED IMPORTED )
set_target_properties(libopencv_reg PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_reg.a")

add_library(libopencv_xobjdetect SHARED IMPORTED )
set_target_properties(libopencv_xobjdetect PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_xobjdetect.a")

add_library(libopencv_text SHARED IMPORTED )
set_target_properties(libopencv_text PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_text.a")

add_library(libopencv_ml SHARED IMPORTED )
set_target_properties(libopencv_ml PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_ml.a")

add_library(libopencv_ccalib SHARED IMPORTED )
set_target_properties(libopencv_ccalib PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_ccalib.a")

add_library(libopencv_objdetect SHARED IMPORTED )
set_target_properties(libopencv_objdetect PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_objdetect.a")

add_library(libopencv_stereo SHARED IMPORTED )
set_target_properties(libopencv_stereo PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_stereo.a")

add_library(libopencv_videostab SHARED IMPORTED )
set_target_properties(libopencv_videostab PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_videostab.a")

add_library(libopencv_aruco SHARED IMPORTED )
set_target_properties(libopencv_aruco PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_aruco.a")

add_library(libopencv_face SHARED IMPORTED )
set_target_properties(libopencv_face PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_face.a")

add_library(libopencv_stitching SHARED IMPORTED )
set_target_properties(libopencv_stitching PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_stitching.a")

add_library(libopencv_phase_unwrapping SHARED IMPORTED )
set_target_properties(libopencv_phase_unwrapping PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_phase_unwrapping.a")

add_library(libopencv_xfeatures2d SHARED IMPORTED )
set_target_properties(libopencv_xfeatures2d PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_xfeatures2d.a")

add_library(libopencv_ximgproc SHARED IMPORTED )
set_target_properties(libopencv_ximgproc PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_ximgproc.a")

add_library(libopencv_shape SHARED IMPORTED )
set_target_properties(libopencv_shape PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_shape.a")

add_library(libopencv_line_descriptor SHARED IMPORTED )
set_target_properties(libopencv_line_descriptor PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_line_descriptor.a")

add_library(libopencv_dpm SHARED IMPORTED )
set_target_properties(libopencv_dpm PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_dpm.a")

add_library(libopencv_flann SHARED IMPORTED )
set_target_properties(libopencv_flann PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_flann.a")

add_library(libopencv_bioinspired SHARED IMPORTED )
set_target_properties(libopencv_bioinspired PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_bioinspired.a")

add_library(libopencv_imgproc SHARED IMPORTED )
set_target_properties(libopencv_imgproc PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_imgproc.a")

add_library(libopencv_optflow SHARED IMPORTED )
set_target_properties(libopencv_optflow PROPERTIES
    IMPORTED_LOCATION "${libs}/${ANDROID_ABI}/libopencv_optflow.a")

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=gnu++11 -fexceptions -frtti")

# Creates and names a library, sets it as either STATIC
# or SHARED, and provides the relative paths to its source code.
# You can define multiple libraries, and CMake builds them for you.
# Gradle automatically packages shared libraries with your APK.

add_library( # Sets the name of the library.
             native-lib

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             src/main/cpp/native-lib.cpp )

# Searches for a specified prebuilt library and stores the path as a
# variable. Because CMake includes system libraries in the search path by
# default, you only need to specify the name of the public NDK library
# you want to add. CMake verifies that the library exists before
# completing its build.

find_library( # Sets the name of the path variable.
              log-lib

              # Specifies the name of the NDK library that
              # you want CMake to locate.
              log )

# Specifies libraries CMake should link to your target library. You
# can link multiple libraries, such as libraries you define in this
# build script, prebuilt third-party libraries, or system libraries.

target_link_libraries( # Specifies the target library.
                       native-lib android log
                       libopencv_saliency
                       libopencv_photo
                       libopencv_bgsegm
                       libopencv_videoio
                       libopencv_surface_matching
                       libopencv_datasets
                       libopencv_calib3d
                       libopencv_xphoto
                       libopencv_features2d
                       libopencv_img_hash
                       libopencv_dnn
                       libopencv_core
                       libopencv_rgbd
                       libopencv_plot
                       libopencv_java3
                       libopencv_imgcodecs
                       libopencv_highgui
                       libopencv_fuzzy
                       libopencv_structured_light
                       libopencv_video
                       libopencv_tracking
                       libopencv_superres
                       libopencv_reg
                       libopencv_xobjdetect
                       libopencv_text
                       libopencv_ml
                       libopencv_ccalib
                       libopencv_objdetect
                       libopencv_stereo
                       libopencv_videostab
                       libopencv_aruco
                       libopencv_face
                       libopencv_stitching
                       libopencv_phase_unwrapping
                       libopencv_xfeatures2d
                       libopencv_ximgproc
                       libopencv_shape
                       libopencv_line_descriptor
                       libopencv_dpm
                       libopencv_flann
                       libopencv_bioinspired
                       libopencv_imgproc
                       libopencv_optflow
                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )