cmake_minimum_required(VERSION 3.12)

project(hello_mate)

add_executable(hello_mate 
    hello_mate.cpp
)

set_target_properties(hello_mate PROPERTIES
    CXX_STANDARD 17
    CXX_STANDARD_REQUIRED ON
)
