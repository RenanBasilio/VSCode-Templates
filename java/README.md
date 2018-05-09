# Java Project Template

This template includes tasks to build a hello world application using Java. It has been tested on Windows and Linux.

## Build Instructions

In order to build the project the Java compiler (`javac`) and archiver (`jar`) must be present on the system PATH.

### VSCode

Invoke the task palette with `ctrl+shift+T` and choose the task `Build` to compile all java files under the `/src` directory. In order to generate an executable archive, edit the `manifest.mf` as necessary and call the `Deploy` task.

The task `Configure` creates the `build` and `target` directories if they do not already exist, while the task `Clean` removes them and their contents.