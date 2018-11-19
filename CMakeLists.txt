cmake_minimum_required(VERSION 3.1)
project(game.libretro.handy)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(HANDY_LIB NAMES handy_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(HANDY_CUSTOM_BINARY ${HANDY_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} HANDY "")

include(CPack)
