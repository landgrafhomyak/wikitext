cmake_minimum_required(VERSION 3.19)
project(wikitext-cpython C)

set(CMAKE_C_STANDARD 90)
set(CMAKE_CXX_STANDARD 98)

add_library(
        wikitext

        src/wikitext.def
        src/init.c
)
target_include_directories(wikitext PUBLIC Include)
set_target_properties(wikitext PROPERTIES OUTPUT_NAME wikitext)

install(TARGETS wikitext)