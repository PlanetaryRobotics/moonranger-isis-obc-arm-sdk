cmake_minimum_required(VERSION 3.5)

project(hcc LANGUAGES C)

set(HCC_ROOT "${CMAKE_CURRENT_SOURCE_DIR}" CACHE STRING "hcc root directory")

add_library(
    ${PROJECT_NAME}
    INTERFACE)
target_include_directories(
    ${PROJECT_NAME}
    INTERFACE
    ${HCC_ROOT}/include/config
    ${HCC_ROOT}/include/hcc
    ${HCC_ROOT}/include/psp/include
    ${HCC_ROOT}/include/version)

