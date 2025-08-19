cmake_minimum_required(VERSION 4.1.0)

project(ogl)

include(FetchContent)
FetchContent_Declare(ogre GIT_REPOSITORY https://github.com/OGRECave/ogre.git GIT_TAG v14.4.0)
FetchContent_MakeAvailable(ogre)

# set(OGRE_DIR "${CMAKE_CURRENT_SOURCE_DIR}/../ogre/ogre_build/cmake/OGRE")
# set(OGRE_MEDIA_DIR "${CMAKE_CURRENT_SOURCE_DIR}/../ogre/Media")
# list(APPEND CMAKE_PREFIX_PATH "${CMAKE_CURRENT_SOURCE_DIR}/../ogre/ogre_build")
# # list(APPEND CMAKE_MODULE_PATH "${CMAKE_CURRENT_SOURCE_DIR}/../../ogre/ogre_build/cmake")

# find_package(OGRE)

add_executable(ogl main.cpp)

# target_link_libraries(wlan kernel32 user32 gdi32 wlanapi)
