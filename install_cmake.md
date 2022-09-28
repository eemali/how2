# How to install CMake?

## Window

1. Download cmake-version-win64-x64.msi OR cmake-win32-x86.msi from <https://cmake.org/download/>
2. Start cmake-version-win64-x64.msi OR cmake-win32-x86.msi
3. Welcome to the CMake setup Wizzard: next
4. End-User License Agreement: [X] Accept and next
5. Install options: [X] Add CMake to the system PATH for all users, next
6. Destination folder: C:\Program Files\CMake (default), next
7. Ready to install CMake, Install

## Linux

1. Download cmake-version-Linux-x86_64.sh from <https://cmake.org/download/>
2. sudo mv cmake-3.15.1-Linux-x86_64.sh /opt
3. cd /opt
4. sudo bash ./cmake-3.15.1-Linux-x86_64.sh
5. sudo ln -s /opt/cmake-3.15.1-Linux-x86_64/bin/* /usr/local/bin/
6. sudo rm cmake-3.15.1-Linux-x86_64.sh
7. restart
8. cmake --version
