if (NOT WIN32)
    add_executable(oceanfx_speed_test "oceanfx_speed_test.c")
    target_link_libraries(oceanfx_speed_test SeaBreeze)
endif()
