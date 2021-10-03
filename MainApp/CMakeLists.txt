cmake_minimum_required(VERSION 3.15)

project(MainApp)

find_package(ClimbingStats REQUIRED)

add_executable(MainApp
    src/main.cpp
)

target_link_libraries(MainApp PRIVATE Upstream::ClimbingStats)
