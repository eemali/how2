# How to build opencv_core using GUI version of CMake for Window/Linux?

1. Create an opencv folder and two sub folders sources and build inside it
2. Download latest OpenCV source code (i.e., opencv-version.zip) from <https://opencv.org/releases/>
3. Extract opencv-version.zip inside opencv/sources
4. Start the GUI version of CMake (`cmake-gui`)
5. Select the folder `opencv/sources` as the source directory
6. Select the folder `opencv/build` as the build directory
7. Press `Configure` button. A window pops up, letting you specify the compiler you want to use
    1. Choose one of following compiler as the generator for project
        - [] Unix Makefiles
        - [] MinGW Makefiles
        - [] Visual Studio xx xxxx
    2. Select “Use default native compilers” and press “Finish” button.
8. Uncheck all except following
    - [x] `BUILD_SHARED_LIBS`
    - [x] `BUILD_opencv_core`
    - [x] `ENABLE_PIC`
9. For Unix or MinGW Makefiles only
    1. For Compilation in Debug mode
        1. Select the folder `opencv/build/install/Debug` in `CMAKE_INSTALL_PREFIX` as the install directory
        2. Select the `CMAKE_BUILD_TYPE` as Debug
    2. For compliance in Release mode
        1. Select the folder `opencv/build/install/` Release in `CMAKE_INSTALL_PREFIX` as the install directory
        2. Select the `CMAKE_BUILD_TYPE` as Release
10. Press `Configure` button again.
11. Press `Generate` button.
12. Open the terminal in opencv/build folder and execute following commands
    1. For Unix or MinGW Makefiles
        ```
        cmake --build . --target install
        ```
    2. For Visual Studio        
        1. For Compilation in Debug mode
        ```
        cmake --build . --config Release --target install
        ```
        2. For compliance in Release mode
        ```
        cmake --build . --config Debug --target install
        ```
