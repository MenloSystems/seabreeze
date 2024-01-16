add_executable(demo-averaging "demo-averaging.c" "util.h" "util.c")
target_link_libraries(demo-averaging SeaBreeze)

add_executable(demo-named-spectrometer "demo-named-spectrometer.c" "util.h" "util.c")
target_link_libraries(demo-named-spectrometer SeaBreeze)

if (NOT WIN32)
    add_executable(demo-pthreads "demo-pthreads.c" "util.h" "util.c")
    target_link_libraries(demo-pthreads SeaBreeze pthread)

    add_executable(demo-qepro-api "demo-qepro-api.c" "util.h" "util.c")
    target_link_libraries(demo-qepro-api SeaBreeze)
endif()

add_executable(demo-raw-usb-seabreezeapi "demo-raw-usb-seabreezeapi.c"  "util.h" "util.c")
target_link_libraries(demo-raw-usb-seabreezeapi SeaBreeze)

add_executable(demo-raw-usb "demo-raw-usb.c" "util.h" "util.c")
target_link_libraries(demo-raw-usb SeaBreeze)

add_executable(demo-stability-scan "demo-stability-scan.c" "util.h" "util.c")
target_link_libraries(demo-stability-scan SeaBreeze)

add_executable(demo-streaming-xml "demo-streaming-xml.c" "util.h" "util.c")
target_link_libraries(demo-streaming-xml SeaBreeze)

add_executable(demo-strobe-sts "demo-strobe-sts.c" "util.h" "util.c")
target_link_libraries(demo-strobe-sts SeaBreeze)

add_executable(demo-strobe "demo-strobe.c" "util.h" "util.c")
target_link_libraries(demo-strobe SeaBreeze)

add_executable(demo-sts-api "demo-sts-api.c" "util.h" "util.c")
target_link_libraries(demo-sts-api SeaBreeze)

add_executable(demo-sts-eeprom "demo-sts-eeprom.c" "util.h" "util.c")
target_link_libraries(demo-sts-eeprom SeaBreeze)

add_executable(demo-timeout "demo-timeout.c" "util.h" "util.c")
target_link_libraries(demo-timeout SeaBreeze pthread)

add_executable(demo-timing "demo-timing.c" "util.h" "util.c")
target_link_libraries(demo-timing SeaBreeze)

add_executable(demo-unformatted-spectrum "demo-unformatted-spectrum.c" "util.h" "util.c")
target_link_libraries(demo-unformatted-spectrum SeaBreeze)

add_executable(seabreeze-util "seabreeze-util.c" "util.h" "util.c")
target_link_libraries(seabreeze-util SeaBreeze)
