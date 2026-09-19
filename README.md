# About
To-do

## Features
To-do

# Running the Program
Requires Java 25 or higher to run.
See releases for instructions on running the standalone JAR. Release versions Alpha 0.0.3 and below have a launch script (VBScript) that is only compatible with Windows systems. However, compiling and running from source works on Windows and Linux, and, although it hasn't been tested, should work on MacOS.

# Compiling and Running from Source

The JavaFX SDK (version 25.0.x) is required to run the project from source.

Download the [JavaFX SDK](https://www.oracle.com/java/technologies/downloads/javafx/#javafx25) and set the module-path in the below JVM arguments to the path of the "lib" folder of the JavaFX SDK. Note that the entire SDK is needed (only having the contents of the lib folder will not work).

For compatibility with [OpenGLFX](https://github.com/husker-dev/openglfx), this program does not use Java 8+ modules. 
To run, add the following JVM arguments:

```
--module-path path/to/javafx/sdk/lib
--add-modules javafx.controls,javafx.graphics,javafx.base,javafx.fxml
--add-exports=javafx.graphics/com.sun.prism=ALL-UNNAMED
--add-exports=javafx.graphics/com.sun.javafx.scene.layout=ALL-UNNAMED
--add-exports=javafx.graphics/com.sun.javafx.scene=ALL-UNNAMED
--add-exports=javafx.graphics/com.sun.javafx.sg.prism=ALL-UNNAMED
--add-exports=javafx.graphics/com.sun.scenario=ALL-UNNAMED
--add-exports=javafx.graphics/com.sun.javafx.tk=ALL-UNNAMED
--add-exports=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED
--enable-native-access=ALL-UNNAMED
--enable-native-access=javafx.graphics
```

Example launch configuration (in launch.json) for VSCode:
(note that vmArgs is a string all on one line containing the above arguments separated by spaces)
```{
    "version": "0.2.0",
    "configurations": [
    {
        "type": "java",
        "name": "Launch App",
        "request": "launch",
        "mainClass": "project.Main",
        "vmArgs": "--module-path path/to/javafx-sdk-25.0.x/lib --add-modules javafx.controls,javafx.graphics,javafx.base,javafx.fxml --add-exports=javafx.graphics/com.sun.prism=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.scene.layout=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.scene=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.sg.prism=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.scenario=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.javafx.tk=ALL-UNNAMED --add-exports=javafx.graphics/com.sun.glass.ui=ALL-UNNAMED --enable-native-access=ALL-UNNAMED --enable-native-access=javafx.graphics"
    }
    ]
```
