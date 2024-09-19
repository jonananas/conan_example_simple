# Simple Conan 1 usage example

## Overview

This project uses Conan to manage dependencies and CMake as the build system. The main dependency is `spdlog`.

## Prerequisites

- [Conan](https://conan.io/downloads.html)
- [CMake](https://cmake.org/download/)
- A C++ compiler (e.g., GCC, Clang, or MSVC)

## Setup

### Step 1: Install Conan

If you don't have Conan installed, you can install it using pip:

```bash
pip install conan
mkdir oos
cd oos
conan install .. --build=missing
cmake ..
ninja
./MyExecutable
```
