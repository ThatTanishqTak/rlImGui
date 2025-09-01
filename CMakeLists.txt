cmake_minimum_required(VERSION 3.10)
project(rlImGui LANGUAGES CXX)

add_library(${PROJECT_NAME} STATIC
    rlImGui.cpp
)

target_include_directories(${PROJECT_NAME} PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/../raylib/src
)

set_target_properties(${PROJECT_NAME} PROPERTIES
    CXX_STANDARD 17
    CXX_STANDARD_REQUIRED ON
)