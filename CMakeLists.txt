project(game.libretro.handy)

cmake_minimum_required(VERSION 2.6)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

enable_language(CXX)

find_package(kodi REQUIRED)
find_package(libretro-handy REQUIRED)

set(HANDY_CUSTOM_BINARY ${HANDY_LIB}
                        ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX} handy)

build_addon(game.libretro.handy HANDY DEPLIBS)
