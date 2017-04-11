cmake_minimum_required(VERSION 3.1)
project(game.libretro.beetle-supergrafx)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-beetle-supergrafx REQUIRED)

set(BEETLE-SUPERGRAFX_CUSTOM_BINARY ${BEETLE-SUPERGRAFX_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} BEETLE-SUPERGRAFX "")
