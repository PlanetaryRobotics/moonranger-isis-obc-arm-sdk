cmake_minimum_required(VERSION 3.5)

project(freertos LANGUAGES C)

set(FREERTOS_DIR ${CMAKE_CURRENT_SOURCE_DIR})
set(FREERTOS_INCLUDE ${FREERTOS_DIR})
file(GLOB FREERTOS_SOURCES ${FREERTOS_DIR}/src/*.c)

add_library(
    ${PROJECT_NAME}
    ${FREERTOS_SOURCES})
target_include_directories(
    ${PROJECT_NAME}
    PUBLIC
    ${FREERTOS_INCLUDE}
    ${FREERTOS_DIR}/include/freertos
    ${FREERTOS_DIR}/include/freertos/portable/GCC/ARM9_AT91SAM9G20
    ${FREERTOS_DIR}/include/freertos/portable/MemMang)
