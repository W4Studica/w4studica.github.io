---
title: Adding W4Studica Libraries
---

## Configure the project for VMX-Pi

If you followed [VS Code Setup](vscode-setup.md), the project is already configured for VMX-Pi. The W4Studica extension connects the project to its compatible prebuilt WPILib and GradleRIO releases and adds the VMX build and deploy support when you select **W4Studica: Change the deploy target to VMX (from SystemCore)**.

You do not need to add dependency blocks or copy library files into `build.gradle` by hand. Keep the project open in WPILib VS Code when using W4Studica commands.

## Build and deploy

Build the robot program on your computer with the Gradle wrapper:

```bash
./gradlew build
```

On Windows, use `gradlew.bat build`. Building compiles the robot project locally. It does not connect to the VMX-Pi to fetch the VMX SDK. Deployment uses the VMX target and requires the robot to be reachable; see [VMX-Pi Network](vmx-pi-network.md).

```bash
./gradlew deploy
```

The VMX connection uses username `ubuntu` and password `password`.

## Use Studica C++ drivers

The VMX project configuration provides the Studica driver and VMX helper headers. For example, the W4Studica VMX C++ sample includes:

```cpp
#include "titan.hpp"
#include "wpi/halsim/vmx/SharedVMX.hpp"
#include "wpi/halsim/vmx/StudicaTitan.hpp"
#include "wpi/halsim/vmx/TitanEnableGuard.hpp"
```

See the [complete VMX C++ example](https://github.com/W4Studica/GradleRIO/tree/main/examples/vmx-cpp) for driver initialization and Driver Station enable handling. Use `wpilibvmx::SharedVMX()` when constructing Studica driver objects so they share the VMX connection. `StudicaTitan` and `TitanEnableGuard` handle the Titan enable state; they do not send motor speed commands for your robot code.

## Optional: Prepare for offline use

To cache the project's dependencies for later offline builds, connect the development computer to the Internet and run **W4Studica: Save W4Studica Offline** from the W4Studica command palette. For a C++ VMX project, the VMX-Pi must also be reachable during the initial SDK setup. This step is only needed when you want to prepare offline builds; an ordinary online `build` does not need the robot.

Run the offline preparation command again after changing the deploy target, updating W4Studica versions, or adding dependencies or vendor libraries.
