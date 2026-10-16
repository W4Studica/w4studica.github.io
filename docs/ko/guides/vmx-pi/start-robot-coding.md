---
title: Start Robot Coding
---

이 페이지에서는 VMX-Pi 및 Studica 라이브러리를 사용하는 C++ 코드를 설명합니다. 먼저 [Adding W4Studica Libraries](adding-w4studica-libraries.md)의 안내대로 프로젝트 배포 대상을 VMX로 설정하세요.

## Studica 헤더 포함하기

VMX 프로젝트 구성에서 다음 헤더를 사용할 수 있습니다. 로봇 코드에서 사용하는 헤더를 포함하세요.

```cpp
#include "titan.hpp"
#include "wpi/halsim/vmx/SharedVMX.hpp"
#include "wpi/halsim/vmx/StudicaTitan.hpp"
#include "wpi/halsim/vmx/TitanEnableGuard.hpp"
```

## VMX 연결 공유하기

Studica 드라이버 객체를 만들 때 `wpilibvmx::SharedVMX()`를 전달하세요. 로봇 코드와 VMX HAL이 같은 VMX 연결을 사용합니다.

Titan에는 `wpilibvmx::StudicaTitan`과 `wpilibvmx::TitanEnableGuard`를 사용하세요. Guard는 Driver Station의 활성 및 E-stop 상태를 따르며 로봇이 비활성화되거나 프로그램이 종료될 때 Titan을 비활성화합니다. 모터 속도 명령은 보내지 않으므로 활성 상태에서 로봇 코드가 계속 명령해야 합니다. 활성 상태 처리를 위해 `studica_driver::Titan::Enable()`을 직접 호출하지 마세요.

객체 초기화, 주기적인 모터 명령, Driver Station 처리는 [VMX C++ 전체 예제](https://github.com/W4Studica/GradleRIO/tree/main/examples/vmx-cpp)를 참고하세요.

빌드·배포와 오프라인 의존성 설정은 [Adding W4Studica Libraries](adding-w4studica-libraries.md) 안내를 참고하세요.
