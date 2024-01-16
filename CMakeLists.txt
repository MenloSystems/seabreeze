cmake_minimum_required(VERSION 3.16)

project(SeaBreeze
        LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 98)

add_library(SeaBreeze SHARED)
target_include_directories(SeaBreeze PUBLIC
    include/
)

# Moved sources to a seperate file to get this massive wall of text out of here
include(sources.cmake)
target_compile_definitions(SeaBreeze PRIVATE BUILD_DLL=1)

if (WIN32)
    target_compile_definitions(SeaBreeze PRIVATE _WINDOWS=1)
    target_link_libraries(SeaBreeze PRIVATE ws2_32 winusb setupapi)
else()
    target_link_libraries(SeaBreeze usb-1.0)
endif()

add_subdirectory(oceanfx_speed_test)
add_subdirectory(sample-code)
