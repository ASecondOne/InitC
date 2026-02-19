# C Project Initializer

A minimal C project initializer inspired by Cargo.  
It creates a ready-to-build C project using CMake with a clean structure and a simple build script.

This tool helps you start new C projects quickly without manually creating folders and configuration files.

---

## Features

- Initializes a complete C project structure
- Uses CMake for portable builds
- Automatically names the project based on the directory name
- Includes a simple build script
- Creates a working Hello World example
- Safe checks to prevent overwriting existing files

---

## Created Structure

After running the initializer:

my_project/

├── CMakeLists.txt 

├── build.sh

└── src/

└── main.c

---

## Requirements

- CMake ≥ 3.15
- A C compiler (gcc, clang, etc.)
- Bash shell

---

## Usage

```bash
./c-init <project-path>
```
Example:
```bash
./c-init hello_world
```

Output:
```bash
Initialized C project at: hello_world
To build: cd "hello_world" && ./build.sh
```
Building the Project
```bash
cd hello_world
./build.sh
```

Output binary will be located in:
```bash
build/hello_world
```

Run it:
```bash
./build/hello_world
```
Example Generated Code
```C
#include <stdio.h>

int main(void) {
    puts("Hello, world!");
    return 0;
}
```
Why use this?

Creating C projects manually involves repetitive steps:

creating folders

writing CMakeLists.txt

configuring builds

setting up structure

This tool automates everything in one command.

Similar to:

cargo init -- But for C.

Possible Future Improvements

-Support for libraries
-Optional Git initialization
-Debug / Release presets
-C++ support
-Testing support
