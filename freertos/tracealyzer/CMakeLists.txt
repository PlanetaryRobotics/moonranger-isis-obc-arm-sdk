cmake_minimum_required(VERSION 3.5)

project(tracealyzer LANGUAGES C)

set(TRACEALYZER_DIR ${CMAKE_CURRENT_SOURCE_DIR})
set(TRACEALYZER_INCLUDES ${TRACEALYZER_DIR}/include)
file(GLOB TRACEALYZER_SOURCES ${TRACEALYZER_DIR}/*.c)

add_library(
    ${PROJECT_NAME}
    ${TRACEALYZER_SOURCES})
target_include_directories(
    ${PROJECT_NAME}
    PUBLIC
    ${TRACEALYZER_INCLUDES})