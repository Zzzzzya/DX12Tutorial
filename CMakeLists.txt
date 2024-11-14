cmake_minimum_required(VERSION 3.29)
project(test)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if(NOT CMAKE_TOOLCHAIN_FILE)
    set(CMAKE_TOOLCHAIN_FILE)
endif()

find_package(fmt CONFIG REQUIRED)

add_executable(test main.cpp)

target_link_libraries(test PRIVATE fmt::fmt)


