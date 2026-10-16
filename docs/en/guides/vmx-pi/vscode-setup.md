---
title: VS Code Setup
---

## Install the W4Studica extension

Open the [W4Studica VS Code Extension releases](https://github.com/W4Studica/W4Studica-VS-Code-Extension/releases) and download the latest `.vsix` file from the release **Assets**. In WPILib VS Code, open the Extensions view, select **…** → **Install from VSIX…**, and choose the downloaded file. After installation, run **W4Studica: Update W4Studica Version** once to configure the extension for your project.

The release page looks like this:

![W4Studica VS Code Extension release page showing the VSIX asset](../../../assets/vscode-extension-release.png)

Use the WPILib-installed VS Code for robot projects so its WPILib tools and extensions are available. For VMX-Pi project setup and deployment, continue with [Adding W4Studica Libraries](adding-w4studica-libraries.md).

## Create a C++ robot project

1. Open the Command Palette with **Ctrl+Shift+P** and run **WPILib: Create a new project**.
2. Set **Template** to **C++**.
3. Select **Command v2 Robot**.
4. Enter your team's assigned number in **Team Number**. Check that it matches your team before continuing.
5. Complete the remaining project fields and select **Create Project**.
6. In the new project, run **W4Studica: Update W4Studica Version** once from the Command Palette. The enlarged view below shows the W4Studica commands.

![Zoomed view of W4Studica commands in the VS Code Command Palette, with the pointer visible](../../../assets/vscode-command-palette-zoom.png)
