cmake_minimum_required(VERSION 3.10)

project(MyProject VERSION 0.0.1)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

add_executable(MyExecutable main.cpp)

include(${CMAKE_BINARY_DIR}/conan_toolchain.cmake)
if(APPLE)
    execute_process(
        COMMAND xcrun --sdk macosx --show-sdk-path
        OUTPUT_VARIABLE CMAKE_OSX_SYSROOT
        OUTPUT_STRIP_TRAILING_WHITESPACE
    )
    set(CMAKE_OSX_SYSROOT ${CMAKE_OSX_SYSROOT} CACHE STRING "" FORCE)
endif()

find_package(spdlog REQUIRED)

target_link_directories(MyExecutable PRIVATE ${CMAKE_LIBRARY_PATH})
target_include_directories(MyExecutable PRIVATE ${CMAKE_INCLUDE_PATH})

target_link_libraries(MyExecutable PRIVATE spdlog::spdlog)
