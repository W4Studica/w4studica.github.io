---
title: VS Code Setup
---

## W4Studica 확장 프로그램 설치

[W4Studica VS Code Extension 릴리스 페이지](https://github.com/W4Studica/W4Studica-VS-Code-Extension/releases)를 열고 최신 릴리스의 **Assets**에서 `.vsix` 파일을 다운로드하세요. WPILib VS Code에서 Extensions 화면을 연 다음 **…** → **Install from VSIX…**를 선택하고 다운로드한 파일을 지정합니다. 설치가 끝나면 **W4Studica: Update W4Studica Version** 명령을 한 번 실행해 프로젝트를 설정하세요.

릴리스 페이지는 아래와 같은 모습입니다.

![VSIX 파일이 표시된 W4Studica VS Code Extension 릴리스 페이지](../../assets/vscode-extension-release.png)

로봇 프로젝트에서는 WPILib 도구와 확장 프로그램이 설치된 WPILib VS Code를 사용하세요. VMX-Pi 프로젝트 구성과 배포 방법은 [Adding W4Studica Libraries](adding-w4studica-libraries.md)를 참고하세요.

## C++ 로봇 프로젝트 만들기

1. **Ctrl+Shift+P**로 명령 팔레트를 열고 **WPILib: Create a new project**를 실행합니다.
2. **Template**에서 **C++**를 선택합니다.
3. 프로젝트 종류로 **Command v2 Robot**을 선택합니다.
4. **Team Number**에 팀에서 사용하는 번호를 입력합니다. 다음 단계로 넘어가기 전에 팀 번호가 정확한지 확인하세요.
5. 나머지 프로젝트 정보를 입력하고 **Create Project**를 선택합니다.
6. 생성된 프로젝트에서 명령 팔레트를 열고 **W4Studica: Update W4Studica Version**을 한 번 실행합니다. 아래 확대 이미지에서 W4Studica 명령을 확인할 수 있습니다.

![마우스 포인터가 보이도록 확대한 VS Code W4Studica 명령 팔레트](../../assets/vscode-command-palette-zoom.png)
