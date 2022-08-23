cmake_minimum_required(VERSION 3.5)

project(at91 LANGUAGES C ASM)

set(AT91_ROOT "${CMAKE_CURRENT_SOURCE_DIR}" CACHE STRING "at91 root directory")

file(GLOB AT91_SOURCES 
    ${AT91_ROOT}/src/*.c 
    ${AT91_ROOT}/src/boards/ISIS_OBC_G20*.c 
    ${AT91_ROOT}/src/boards/ISIS_OBC_G20/at91sam9g20/*.S
    ${AT91_ROOT}/src/memories/*.c 
    ${AT91_ROOT}/src/peripherals/*.c
    ${AT91_ROOT}/src/usb/*.c
    ${AT91_ROOT}/src/utility/*.c
    )

add_library(
    ${PROJECT_NAME}
    ${AT91_SOURCES}
    )
target_include_directories(
    ${PROJECT_NAME}
    INTERFACE
    ${AT91_ROOT}/include/boards/ISIS_OBC_G20
    ${AT91_ROOT}/include/boards/ISIS_OBC_G2/at91sam9g20
    ${AT91_ROOT}/include/memories
    ${AT91_ROOT}/include/peripherals/pit/
    ${AT91_ROOT}/include/usb
    ${AT91_ROOT}/include/utility
    ${AT91_ROOT}/include)

