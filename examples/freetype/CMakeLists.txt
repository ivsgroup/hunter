# Copyright (c) 2015, Ruslan Baratov
# All rights reserved.

cmake_minimum_required(VERSION 3.0)

# Emulate HunterGate:
# * https://github.com/hunter-packages/gate
include("../common.cmake")

project(download-freetype)

# download freetype
hunter_add_package(freetype)

# now freetype can be used
find_package(freetype CONFIG REQUIRED)

add_executable(foo foo.cpp)
target_link_libraries(foo freetype::freetype)
