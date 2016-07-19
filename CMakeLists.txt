cmake_minimum_required(VERSION 2.8)
project(sdl2pp_msvc2015)

set(SDL2PP_WITH_IMAGE ON)
set(SDL2PP_WITH_MIXER ON)
set(SDL2PP_WITH_TTF ON)
add_subdirectory(extlibs/libSDL2pp)
