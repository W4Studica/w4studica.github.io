---
title: VS Code Setup
---

## W4Studica 확장 프로그램 설치

1. [W4Studica VS Code Extension 릴리스 페이지](https://github.com/W4Studica/W4Studica-VS-Code-Extension/releases)를 열고 최신 릴리스의 **Assets**에서 `.vsix` 파일을 다운로드합니다.

   ![VSIX 파일이 표시된 W4Studica VS Code Extension 릴리스 페이지](../../assets/vscode-extension-release.png)

2. WPILib VS Code에서 **Extensions** 화면을 열고 **…** → `Install from VSIX…`를 선택합니다.

   ![Extensions 메뉴에서 Install from VSIX를 선택하는 화면과 마우스 포인터 확대](../../assets/vscode-install-menu-zoom.png)

3. 다운로드한 `.vsix` 파일을 선택하고 **Install**을 누릅니다.

   ![파일 선택 창에서 다운로드한 vmxpi-wsr VSIX를 선택한 모습](../../assets/vscode-file-picker-zoom.png)

4. W4Studica 프로젝트 명령을 사용하려면 먼저 WPILib 로봇 프로젝트를 만들거나 열어야 합니다. 프로젝트가 열려 있을 때만 이 명령들을 사용할 수 있습니다.

로봇 프로젝트에서는 WPILib 도구와 확장 프로그램이 설치된 WPILib VS Code를 사용하세요. VMX-Pi 프로젝트 구성과 배포 방법은 [Adding W4Studica Libraries](adding-w4studica-libraries.md)를 참고하세요.

## C++ 로봇 프로젝트 만들기

1. **Ctrl+Shift+P**로 명령 팔레트를 열고 **WPILib: Create a new project**를 실행합니다.

   ![마우스 포인터가 가리키는 WPILib Create a new project 명령](../../assets/vscode-create-project-command-zoom.png)
2. **Template**에서 `C++`를 선택합니다.
3. 프로젝트 종류로 **Command v2 Robot**을 선택합니다.
4. **Team Number**에 팀에서 사용하는 번호를 입력합니다. 다음 단계로 넘어가기 전에 팀 번호가 정확한지 확인하세요.
5. 나머지 프로젝트 정보를 입력하고 **Create Project**를 선택합니다.

   프로젝트가 WPILib VS Code에서 열립니다. 아래 캡처에는 프로젝트 생성 후 빌드 성공 화면도 보입니다.

   ![WPILib VS Code에서 열린 프로젝트와 빌드 성공 화면](../../assets/vscode-project-created.png)
6. 생성된 프로젝트를 연 상태에서 명령 팔레트를 열고 **W4Studica: Change the deploy target to VMX (from SystemCore)**를 선택합니다. 아래 캡처에서 노란 테두리와 화살표가 VMX 대상 명령을 가리킵니다.

   ![노란색으로 VMX 배포 대상 명령을 강조한 명령 팔레트](../../assets/vscode-command-palette-zoom.png)

**Update W4Studica Version**은 다른 기능입니다. 열린 프로젝트에 사용할 수 있는 최신 W4Studica 라이브러리 버전을 내려받아 고정할 때 사용하며, 배포 대상을 VMX로 바꾸지는 않습니다. 라이브러리 버전을 업데이트할 때만 실행하세요.
