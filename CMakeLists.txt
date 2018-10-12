cmake_minimum_required(VERSION 3.4)
project (libgl3w)

add_library(libgl3w
    STATIC
    src/gl3w.c
)

target_include_directories(libgl3w
    PUBLIC
    include
)

target_link_libraries(libgl3w
    PUBLIC
    ${CMAKE_DL_LIBS}
)
