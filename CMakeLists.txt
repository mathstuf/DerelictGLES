cmake_minimum_required(VERSION 2.8.12)
project(DerelictGLES D)
list(APPEND CMAKE_MODULE_PATH
    "${CMAKE_CURRENT_SOURCE_DIR}/cmake")

find_package(Derelict REQUIRED
    COMPONENTS
        util)

include_directories("${CMAKE_CURRENT_SOURCE_DIR}/source")
add_library(DerelictGLES STATIC
    source/derelict/gles/constants2.d
    source/derelict/gles/egl.d
    source/derelict/gles/eglext.d
    source/derelict/gles/eglplatform.d
    source/derelict/gles/egltypes.d
    source/derelict/gles/ext2.d
    source/derelict/gles/functions2.d
    source/derelict/gles/internal.d
    source/derelict/gles/gles2.d
    source/derelict/gles/types2.d)
target_link_libraries(DerelictGLES
    Derelict::util)
