cmake_minimum_required(VERSION 3.1)
project(game.libretro.handy)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-handy REQUIRED)

set(HANDY_CUSTOM_BINARY ${HANDY_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} HANDY "")

include(CPack)
