cmake_minimum_required(VERSION 2.8)
project(sdl2pp_msvc2015)

add_subdirectory(extlibs/libSDL2pp)
include_directories(SYSTEM ${SDL2PP_INCLUDE_DIRS})

find_library(SDL2MAIN_LIBRARY NAMES SDL2main)
set(SDL2PP_LIBRARIES ${SDL2MAIN_LIBRARY} ${SDL2PP_LIBRARIES})

add_executable(sdl2pp_msvc2015 main.cpp)
target_link_libraries(sdl2pp_msvc2015 winmm.lib ${SDL2PP_LIBRARIES})
