# OpenCV Android Library

In order to build the aar library file, firstly we need to build opencv files:

## Preparation
* Update submodule project: opencv and opencv_contrib

* Install Android Studio and install necessary components of Android from Android Studio
    * https://developer.android.com/studio/index.html
* Download Android NDK r10e from: https://developer.android.com/ndk/downloads/older_releases.html
    * Linux: https://dl.google.com/android/repository/android-ndk-r10e-linux-x86_64.zip
    * Mac: https://dl.google.com/android/repository/android-ndk-r10e-darwin-x86_64.zip
    * P.S. Current opencv (3.4.0) only support up to ndk r10.
* Download Android sdk tools version 25.2.5, overwrite `tools` folder inside android sdk folder.
    * Linux: https://dl.google.com/android/repository/tools_r25.2.5-linux.zip
    * Mac: https://dl.google.com/android/repository/tools_r25.2.5-macosx.zip
    * P.S. After version 25.5.2, `android` command is deleted which is used by opencv build script.
* Install cmake, ninja, ant
    * Ubuntu: sudo apt install cmake ninja-build ant
    * Mac: brew install cmake ninja ant

## Build
* Assume directories are as follows:
    * ndk: ~/android-ndk-r10e
    * sdk: ~/Android/Sdk
        * Default sdk directory:
            * Linux: ~/Android/Sdk
            * Mac: ~/Library/Android/sdk
* Enter dir: fingerprint-frontend/opencv-library

* If got error `CMake was unable to find a build program corresponding to "Ninja"` on Mac, we need to modify ./opencv/platforms/android/build_sdk.py:
    
```diff
def build_library(self, abi, do_install):
        cmd = [
            "cmake",
            "-GNinja",
            "-DCMAKE_TOOLCHAIN_FILE='%s'" % self.get_toolchain_file(),
            "-DWITH_OPENCL=OFF",
            "-DWITH_CUDA=OFF",
            "-DWITH_IPP=%s" % ("ON" if abi.haveIPP() else "OFF"),
            "-DBUILD_EXAMPLES=OFF",
            "-DBUILD_TESTS=OFF",
            "-DBUILD_PERF_TESTS=OFF",
            "-DBUILD_DOCS=OFF",
            "-DBUILD_ANDROID_EXAMPLES=ON",
            "-DINSTALL_ANDROID_EXAMPLES=ON",
            "-DANDROID_STL=gnustl_static",
            "-DANDROID_NATIVE_API_LEVEL=9",
            "-DANDROID_ABI='%s'" % abi.cmake_name,
            "-DWITH_TBB=ON",
-           "-DANDROID_TOOLCHAIN_NAME=%s" % abi.toolchain
+           "-DANDROID_TOOLCHAIN_NAME=%s" % abi.toolchain,
+           "-DCMAKE_MAKE_PROGRAM=%s" % "/usr/local/bin/ninja"
         ]
```
```diff
    def build_engine(self, abi, engdest):
        cmd = [
            "cmake",
            "-GNinja",
            "-DCMAKE_TOOLCHAIN_FILE='%s'" % self.get_toolchain_file(),
            "-DANDROID_ABI='%s'" % abi.cmake_name,
            "-DBUILD_ANDROID_SERVICE=ON",
            "-DANDROID_PLATFORM_ID=%s" % abi.platform_id,
            "-DWITH_CUDA=OFF",
            "-DWITH_OPENCL=OFF",
            "-DWITH_IPP=OFF",
            "-DWITH_CUDA=OFF",
            "-DWITH_OPENCL=OFF",
            "-DWITH_IPP=OFF",
+           "-DCMAKE_MAKE_PROGRAM=%s" % "/usr/local/bin/ninja",
             self.opencvdir
         ]
```
    
* run the build script:

```shell
mkdir build
./opencv/platforms/android/build_sdk.py --ndk_path ~/android-ndk-r10e --sdk_path ~/Android/Sdk --extra_modules_path ./opencv_contrib/modules ./build ./opencv
```

### Reference
http://yangchao.me/post/build-opencv-android-sdk/
