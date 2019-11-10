cmake_minimum_required(VERSION 3.4)
project (libgl3w)

option(LIBGL3W_BUILD_SHARED "Build shared lib" OFF)

if (LIBGL3W_BUILD_SHARED)
    add_library(libgl3w
        SHARED
        src/gl3w.c
    )
else()
    add_library(libgl3w
        STATIC
        src/gl3w.c
    )
endif()

target_include_directories(libgl3w
    PUBLIC
    include
)

target_link_libraries(libgl3w
    PRIVATE
    ${CMAKE_DL_LIBS}
)
