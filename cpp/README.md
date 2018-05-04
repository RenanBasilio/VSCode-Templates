# C++ Template Project

This template includes tasks to build a hello world application using CMake 3.9 or higher. It has been tested on Windows and Linux.

## Build Instructions

In order to build the project CMake and a compiler supported by it are required.

### VSCode

Invoke the task palette with `ctrl+shift+T` and choose the task `Make` to create the build scripts with CMake, then once again with the task `Build` for the configuration of choice (Debug or Release).

### Terminal

Execute the following commands from the root directory of the project:

```
cmake . -Bbuild
cmake --build build --config Release
```