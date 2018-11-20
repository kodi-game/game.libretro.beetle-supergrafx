cmake_minimum_required(VERSION 3.1)
project(game.libretro.beetle-supergrafx)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_library(BEETLE-SUPERGRAFX_LIB NAMES mednafen_supergrafx_libretro${CMAKE_SHARED_LIBRARY_SUFFIX} PATH_SUFFIXES libretro)

set(BEETLE-SUPERGRAFX_CUSTOM_BINARY ${BEETLE-SUPERGRAFX_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BEETLE-SUPERGRAFX "")

include(CPack)
