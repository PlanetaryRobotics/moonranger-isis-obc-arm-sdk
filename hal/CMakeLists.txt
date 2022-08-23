cmake_minimum_required(VERSION 3.5)

project(hal LANGUAGES C)

set(HAL_ROOT "${CMAKE_CURRENT_SOURCE_DIR}" CACHE STRING "hal root directory")

add_library(
    ${PROJECT_NAME}
    INTERFACE)
target_include_directories(
    ${PROJECT_NAME}
    INTERFACE
    ${HAL_ROOT}/include
    ${HAL_ROOT}/include/hal/Drivers
    ${HAL_ROOT}/include/hal/Storage
    ${HAL_ROOT}/include/hal/Timing
    ${HAL_ROOT}/include/hal/Utility
    ${HAL_ROOT}/include/version)

