# Simple Conan usage example

This CMake project uses Conan to manage dependencies. The example dependency is `spdlog`.
Works both for conan 1 and conan 2, but for conan 2 you need to create a profile. Just follow the instructions from conan.

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
conan install .. --build=missing
cmake .. -DCMAKE_BUILD_TYPE=Release
ninja
./MyExecutable
```
