# Compile OGRE
# cmake -DCMAKE_INSTALL_PREFIX=C:\reirina\dev-llvm\deps -DBUILD_SHARED_LIBS=OFF -DOGRE_STATIC=ON -DOGRE_DEPENDENCIES_DIR=C:\reirina\dev-llvm\deps -DCMAKE_BUILD_TYPE=Release ..
# cmake --build . --config Release --target install
# the --config must match -DCMAKE_BUILD_TYPE when compile with xcode and MSVC

# Compile Project using OGRE
# cmake -DOGRE_STATIC=ON -DCMAKE_BUILD_TYPE=Release ..
# cmake --build . --config Release


cmake_minimum_required(VERSION 4.1.0)

project(ogl)

set(OGRE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/../deps/CMake/OGRE")
# set(OGRE_MEDIA_DIR "${CMAKE_CURRENT_SOURCE_DIR}/../ogre/Media")
list(APPEND CMAKE_PREFIX_PATH "${CMAKE_CURRENT_SOURCE_DIR}/../deps")
list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/../../deps/CMake")

# find_package(OGRE)
find_package(OGRE REQUIRED COMPONENTS Bites CONFIG)

add_executable(ogl main.cpp)

target_link_libraries(ogl OgreBites)
# target_link_libraries(wlan kernel32 user32 gdi32 wlanapi)
