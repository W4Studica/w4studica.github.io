---
title: Start Robot Coding
---

This page covers the C++ code that uses the VMX-Pi and Studica libraries. Set the project to the VMX target first, as described in [Adding W4Studica Libraries](adding-w4studica-libraries.md).

## Include the Studica headers

The VMX project setup provides these headers. Include the ones used by your robot code:

```cpp
#include "titan.hpp"
#include "wpi/halsim/vmx/SharedVMX.hpp"
#include "wpi/halsim/vmx/StudicaTitan.hpp"
#include "wpi/halsim/vmx/TitanEnableGuard.hpp"
```

## Use the shared VMX connection

Pass `wpilibvmx::SharedVMX()` when constructing Studica driver objects. This gives robot code and the VMX HAL the same VMX connection.

For a Titan, use `wpilibvmx::StudicaTitan` with `wpilibvmx::TitanEnableGuard`. The guard follows the Driver Station enabled and E-stop state and disables the Titan when the robot is disabled or the program stops. It does not send motor speed commands; your robot code must continue sending those while enabled. Do not call `studica_driver::Titan::Enable()` directly for enable-state handling.

See the [complete VMX C++ example](https://github.com/W4Studica/GradleRIO/tree/main/examples/vmx-cpp) for object initialization, periodic motor commands, and Driver Station handling.

For build, deploy, and offline dependency setup, return to [Adding W4Studica Libraries](adding-w4studica-libraries.md).
