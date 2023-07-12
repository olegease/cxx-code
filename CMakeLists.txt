# Ⓒ 2023 - Oleg'Ease'Kharchuk
# from  3.8 available C++17
# from 3.12 available C++20
# from 3.20 available C++23
cmake_minimum_required(VERSION 3.8)

# LANGUAGES C CXX are enabled by default
project(ProjectName VERSION 0.0.0)

# library or executable?
add_library(${PROJECT_NAME} source/lib.c)
#add_executable(${PROJECT_NAME} source/main.cxx)
target_compile_features(${PROJECT_NAME}
    PRIVATE cxx_std_17
    PRIVATE c_std_11
)
# build libraries
#add_subdirectory(submodules)
#add_subdirectory(libs)
add_subdirectory(libs/c-corelib)

target_include_directories(${PROJECT_NAME}
    PUBLIC include
    PRIVATE source
)

target_link_libraries(${PROJECT_NAME} ease::c-corelib)

# build examples projects
add_subdirectory(examples)

# testing
enable_testing()
add_subdirectory(tests)
