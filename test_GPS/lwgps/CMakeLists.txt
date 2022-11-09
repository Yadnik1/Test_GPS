add_library(lwgps INTERFACE)
target_sources(lwgps INTERFACE
    ${CMAKE_CURRENT_LIST_DIR}/src/include/lwgps.h
    ${CMAKE_CURRENT_LIST_DIR}/src/include/lwgps_opts.h
    ${CMAKE_CURRENT_LIST_DIR}src/lwgps/lwgps.c

)
target_include_directories(lwgps INTERFACE
        lwgps
        include
)
target_link_libraries(lwgps INTERFACE
        hardware_spi
        hardware_dma
        hardware_rtc
        pico_stdlib
        hardware_gpio
        hardware_uart
)
