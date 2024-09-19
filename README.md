# Simple Conan usage example

This CMake project uses Conan to manage dependencies. The example dependency is `spdlog`.
Works both for conan 1 and conan 2, but for conan 2 you need to create a profile - follow the instructions from conan if you do not have a profile already.

## Prerequisites

NOTE: Only tested on OSX so far!

- [Conan](https://conan.io/downloads.html)
  - If you don't have Conan installed, you can install it using pip: `pip install conan`
- [CMake](https://cmake.org/download/)
- A C++ compiler (e.g., GCC, Clang, or MSVC)

## Build

```bash
mkdir oos
cd oos
conan install .. --build=missing --output-folder .
cmake .. -DCMAKE_BUILD_TYPE=Release
ninja
./MyExecutable
```

## Poetry

Poetry configuration for isolating conan2 in a virtual environment is provided.
Run `poetry shell` before build commands.
