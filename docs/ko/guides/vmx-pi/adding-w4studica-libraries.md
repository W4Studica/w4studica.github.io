---
title: Adding W4Studica Libraries
---

## VMX-Pi용 프로젝트 구성

[VS Code Setup](vscode-setup.md)의 안내를 따라왔다면 프로젝트는 이미 VMX-Pi용으로 설정되어 있습니다. W4Studica 확장 프로그램에서 **W4Studica: Change the deploy target to VMX (from SystemCore)**를 선택하면 호환되는 사전 빌드 WPILib 및 GradleRIO 릴리스가 연결되고 VMX 빌드·배포 지원이 프로젝트에 추가됩니다.

`build.gradle`에 의존성 블록을 직접 추가하거나 라이브러리 파일을 프로젝트에 복사할 필요가 없습니다. W4Studica 명령을 사용할 때는 WPILib VS Code에서 프로젝트를 열어 두세요.

## 빌드 및 배포

Gradle Wrapper로 컴퓨터에서 로봇 프로그램을 빌드합니다.

```bash
./gradlew build
```

Windows에서는 `gradlew.bat build`를 사용하세요. 빌드는 로봇 프로젝트를 개발 컴퓨터에서 컴파일하며 VMX-Pi에 연결해 VMX SDK를 가져오지 않습니다. 배포하려면 VMX 대상이 설정되어 있어야 하고 로봇에 연결할 수 있어야 합니다. 네트워크 설정은 [VMX-Pi Network](vmx-pi-network.md)를 참고하세요.

```bash
./gradlew deploy
```

VMX 연결에는 사용자 이름 `ubuntu`, 비밀번호 `password`를 사용합니다.

## Studica C++ 드라이버 사용

VMX 프로젝트 구성에서 Studica 드라이버와 VMX 헬퍼 헤더를 사용할 수 있습니다. 예를 들어 W4Studica VMX C++ 샘플은 다음 헤더를 포함합니다.

```cpp
#include "titan.hpp"
#include "wpi/halsim/vmx/SharedVMX.hpp"
#include "wpi/halsim/vmx/StudicaTitan.hpp"
#include "wpi/halsim/vmx/TitanEnableGuard.hpp"
```

드라이버 초기화와 Driver Station 활성화 처리는 [VMX C++ 전체 예제](https://github.com/W4Studica/GradleRIO/tree/main/examples/vmx-cpp)를 참고하세요. Studica 드라이버 객체를 만들 때는 `wpilibvmx::SharedVMX()`를 전달해 VMX 연결을 공유해야 합니다. `StudicaTitan`과 `TitanEnableGuard`는 Titan 활성 상태를 처리하며, 로봇 코드에서 모터 속도를 명령하는 부분은 별도로 작성해야 합니다.

## 선택 사항: 오프라인 사용 준비

나중에 오프라인 빌드를 할 수 있도록 프로젝트 의존성을 캐시하려면 개발 컴퓨터를 인터넷에 연결한 상태에서 W4Studica 명령 팔레트의 **W4Studica: Save W4Studica Offline**을 실행하세요. C++ VMX 프로젝트는 최초 SDK 설정 중 VMX-Pi에도 연결할 수 있어야 합니다. 이 과정은 오프라인 빌드를 준비할 때만 필요하며, 일반적인 온라인 `build`에는 로봇 연결이 필요하지 않습니다.

배포 대상을 바꾸거나 W4Studica 버전을 업데이트하거나 의존성·벤더 라이브러리를 추가한 뒤에는 오프라인 준비 명령을 다시 실행하세요.
