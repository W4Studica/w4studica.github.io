---
title: Adding W4Studica Libraries
---

## C++ 로봇 프로젝트 만들기

1. **Ctrl+Shift+P**로 명령 팔레트를 열고 **WPILib: Create a new project**를 실행합니다.

   ![마우스 포인터가 가리키는 WPILib Create a new project 명령](../../assets/vscode-create-project-command-zoom.png)
2. **Template**에서 `C++`를 선택합니다.
3. 프로젝트 종류로 **Command v2 Robot**을 선택합니다.
4. **Team Number**에 팀에서 사용하는 번호를 입력합니다. 다음 단계로 넘어가기 전에 팀 번호가 정확한지 확인하세요.
5. 나머지 프로젝트 정보를 입력하고 **Create Project**를 선택합니다.

   프로젝트가 열리면 빌드를 실행해 성공하는지 확인합니다. 아래 캡처에 **BUILD SUCCESSFUL** 결과가 보입니다.

   ![WPILib VS Code 터미널의 BUILD SUCCESSFUL 결과](../../assets/vscode-build-success.png)
6. 프로젝트를 연 상태에서 편집기 도구 모음의 **W4Studica** 아이콘을 클릭해 W4Studica 명령 팔레트를 엽니다. 아래 캡처에서 포인터가 W4Studica 아이콘 위에 있고, 툴팁에 “Open W4Studica Command Palette”라고 표시됩니다.

   ![명령 팔레트 툴팁과 함께 포인터가 올라간 W4Studica 도구 모음 아이콘](../../assets/vscode-w4studica-icon-click.png)
7. **W4Studica: Change the deploy target to VMX (from SystemCore)**를 선택합니다. 아래 캡처에서 노란 테두리와 화살표가 VMX 대상 명령을 가리킵니다.

   ![노란색으로 VMX 배포 대상 명령을 강조한 명령 팔레트](../../assets/vscode-command-palette-zoom.png)


## 선택 사항: W4Studica 라이브러리 버전 업데이트

프로젝트가 열린 상태에서 **W4Studica: Update W4Studica Version**을 실행하면 해당 프로젝트에 사용할 수 있는 최신 W4Studica 라이브러리 버전을 내려받아 고정합니다. 이 명령은 별도의 선택적 유지 관리 기능이며, 배포 대상을 VMX로 바꾸지는 않습니다.

## W4Studica 라이브러리 구성

위 프로젝트 설정에서 **W4Studica: Change the deploy target to VMX (from SystemCore)**를 선택하면 호환되는 사전 빌드 WPILib 및 GradleRIO 릴리스가 연결되고 VMX 빌드·배포 지원이 프로젝트에 추가됩니다. `build.gradle`에 의존성 블록을 직접 추가하거나 라이브러리 파일을 프로젝트에 복사할 필요가 없습니다. W4Studica 명령을 사용할 때는 WPILib VS Code에서 프로젝트를 열어 두세요.

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

C++ 헤더와 로봇 코드 예제는 [Start Robot Coding](start-robot-coding.md)에서 확인하세요.

## 선택 사항: 오프라인 사용 준비

나중에 오프라인 빌드를 할 수 있도록 프로젝트 의존성을 캐시하려면 개발 컴퓨터를 인터넷에 연결한 상태에서 W4Studica 명령 팔레트의 **W4Studica: Save W4Studica Offline**을 실행하세요. C++ VMX 프로젝트는 최초 SDK 설정 중 VMX-Pi에도 연결할 수 있어야 합니다. 이 과정은 오프라인 빌드를 준비할 때만 필요하며, 일반적인 온라인 `build`에는 로봇 연결이 필요하지 않습니다.

배포 대상을 바꾸거나 W4Studica 버전을 업데이트하거나 의존성·벤더 라이브러리를 추가한 뒤에는 오프라인 준비 명령을 다시 실행하세요.
