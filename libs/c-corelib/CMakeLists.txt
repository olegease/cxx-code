cmake_minimum_required(VERSION 3.8)

project(c-corelib LANGUAGES C)

add_library(${PROJECT_NAME} source/c-corelib.c)
add_library(ease::${PROJECT_NAME} ALIAS ${PROJECT_NAME})

target_include_directories(${PROJECT_NAME} 
    PUBLIC include
    PRIVATE source
)
