option(BUILD_EXAMPLES "Build Examples" ON)

if (NOT BUILD_EXAMPLES)
    return()
endif()

add_subdirectory(c)
add_subdirectory(cpp)
