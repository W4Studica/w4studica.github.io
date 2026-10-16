---
title: VS Code Setup
---

## Install the W4Studica extension

1. Open the [W4Studica VS Code Extension releases](https://github.com/W4Studica/W4Studica-VS-Code-Extension/releases) and download the latest `.vsix` file from the release **Assets**.

   ![W4Studica VS Code Extension release page showing the VSIX asset](../../../assets/vscode-extension-release.png)

2. In WPILib VS Code, click the **Extensions** icon in the Activity Bar. The screenshot shows the pointer on that icon.

   ![WPILib VS Code Extensions icon with the mouse pointer over it](../../../assets/vscode-extensions-icon-zoom.png)

3. Select **…** in the Extensions view, then choose **Install from VSIX…**.

   ![The Extensions menu with Install from VSIX highlighted and the mouse pointer visible](../../../assets/vscode-install-menu-zoom.png)

4. Select the `.vsix` file you downloaded and click **Install**.

   ![The downloaded vmxpi-wsr VSIX selected in the file picker](../../../assets/vscode-file-picker-zoom.png)

Next, create a WPILib robot project below. Keep the project open when you choose the VMX deploy target; W4Studica project commands are available only while a project is open. Use WPILib-installed VS Code so the WPILib tools and extensions are available.

## Create a C++ robot project

1. Open the Command Palette with **Ctrl+Shift+P** and run **WPILib: Create a new project**.

   ![WPILib Create a new project command with the pointer over it](../../../assets/vscode-create-project-command-zoom.png)
2. Set **Template** to **C++**.
3. Select **Command v2 Robot**.
4. Enter your team's assigned number in **Team Number**. Check that it matches your team before continuing.
5. Complete the remaining project fields and select **Create Project**.

   After the project opens, run a build and confirm that it succeeds. The screenshot shows **BUILD SUCCESSFUL**.

   ![WPILib VS Code terminal showing BUILD SUCCESSFUL](../../../assets/vscode-build-success.png)
6. With the project open, click the **W4Studica** icon in the editor toolbar to open its Command Palette. The screenshot shows the pointer on the W4Studica icon; the tooltip reads “Open W4Studica Command Palette.”

   ![Mouse pointer over the W4Studica toolbar icon, with its Command Palette tooltip visible](../../../assets/vscode-w4studica-icon-click.png)
7. Select **W4Studica: Change the deploy target to VMX (from SystemCore)**. The yellow outline and arrow in the screenshot mark this VMX target command.

   ![Command Palette with the VMX deploy-target command outlined in yellow](../../../assets/vscode-command-palette-zoom.png)

## Optional: Update W4Studica library versions

With a project open, **W4Studica: Update W4Studica Version** downloads and pins the newest compatible W4Studica library versions for that project. This is a separate, optional maintenance command; it does not switch the deploy target.
