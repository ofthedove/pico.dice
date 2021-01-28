cmake_minimum_required(VERSION 3.12)

include(pico_sdk_import.cmake)

project(dice_project)

pico_sdk_init()

add_executable(dice
   dice.c
)

pico_enable_stdio_usb(dice 1)
pico_enable_stdio_uart(dice 1)

pico_add_extra_outputs(dice)

target_link_libraries(dice pico_stdlib)
