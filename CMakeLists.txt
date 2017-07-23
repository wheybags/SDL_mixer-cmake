CMAKE_MINIMUM_REQUIRED(VERSION 3.0)

PROJECT(SDL_mixer VERSION 2.0.1)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake/")
find_package(SDL2 REQUIRED)

set(SRC_C_FILES
    dynamic_flac.c
    dynamic_fluidsynth.c
    dynamic_mod.c
    dynamic_modplug.c
    dynamic_mp3.c
    dynamic_ogg.c
    effect_position.c
    effect_stereoreverse.c
    effects_internal.c
    fluidsynth.c
    load_aiff.c
    load_flac.c
    load_mp3.c
    load_ogg.c
    load_voc.c
    mixer.c
    music.c
    music_cmd.c
    music_flac.c
    music_mad.c
    music_mod.c
    music_modplug.c
    music_ogg.c
    wavestream.c
)

set(SRC_H_FILES
    dynamic_flac.h
    dynamic_fluidsynth.h
    dynamic_mod.h
    dynamic_modplug.h
    dynamic_mp3.h
    dynamic_ogg.h
    effects_internal.h
    fluidsynth.h
    load_aiff.h
    load_flac.h
    load_mp3.h
    load_ogg.h
    load_voc.h
    music_cmd.h
    music_flac.h
    music_mad.h
    music_mod.h
    music_modplug.h
    music_ogg.h
    SDL_mixer.h
    wavestream.h
)

set(SRC_FILES ${SRC_C_FILES} ${SRC_H_FILES})

add_library(SDL_mixer ${SRC_FILES})

link_libraries(${SDL2_LIBRARY})
include_directories(${SDL2_INCLUDE_DIR})
