cmake_minimum_required (VERSION 3.6)

project ("JoyShockLibrary" CXX)

include (cmake/LinuxConfig.cmake)
include (cmake/WindowsConfig.cmake)

if (BUILD_SHARED_LIBS)
    set (JSL_PLATFORM_DEPENDENCY_VISIBILITY PRIVATE)
else ()
    set (JSL_PLATFORM_DEPENDENCY_VISIBILITY PUBLIC)
endif ()

add_subdirectory (JoyShockLibrary)
