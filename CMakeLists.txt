# Specify the minimum required version of CMake
cmake_minimum_required(VERSION 3.10)

# Set the project name and version
project(MyProject VERSION 1.0)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add the executable target
add_executable(MyExecutable main.cpp)

# Include directories if necessary
# include_directories(${PROJECT_SOURCE_DIR}/include)

# Link libraries if necessary
# target_link_libraries(MyExecutable PRIVATE my_library)
