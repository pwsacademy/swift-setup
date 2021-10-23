# Windows 10 / 11

The following instructions will help you get started with Swift on Windows. Two installation methods are available:

- Manually download Swift and its dependencies
- Use the Windows Package Manager (**winget**)

## Prerequisites

Before you install Swift, first enable **developer mode**. This is required for the Swift Package Manager to work properly.

On Windows 10, open the **Start** menu and navigate to **Settings ▸ Update & Security ▸ For developers**. Here, you can enable developer mode:

![](developer-mode-10.png)

On Windows 11, you can find this setting under **Settings ▸ Privacy & security ▸ For developers**:

![](developer-mode-11.png)

Next, proceed with one of the following two installation methods.

## Option 1: Manual downloads

First, download and install [**Visual Studio 2019**](https://visualstudio.microsoft.com), which is Microsoft’s IDE for development on Windows. Although you won’t use Visual Studio to develop Swift applications, you’ll need some of the tools and libraries that come with it.

If you don’t already use Visual Studio, install the free community edition:

![](visual-studio.png)

During installation, select the latest versions of the following **individual components**:

- Git for Windows
- MSVC v142 - VS 2019 C++ x64/x86 build tools
- Python 3 64-bit
- Windows Universal C Runtime
- Windows 10 SDK

These are the only Visual Studio components you need for Swift development. If Visual Studio prompts you about installing workloads, it’s safe to continue without adding any:

![](visual-studio-workloads.png)

Next, download and install the latest [release](https://swift.org/download/#releases) of Swift for Windows 10. You’ll see some security warnings during installation; this is normal:

![](security-warning.png)

Click **More info**, then **Run anyway** to run the installer.

After installing Swift, open **Command Prompt** and verify that you can run the following command:

```
swift --version
```

## Option 2: Windows Package Manager

First, install or update **App Installer** from the Microsoft Store:

![](app-installer.png)

This will make sure you have the Windows Package Manager (**winget**) installed.

Next, open **Command Prompt** and run the following commands:

```
winget install --id Git.Git
winget install --id Python.Python.3 --version 3.7.8150.0
curl -sOL https://aka.ms/vs/16/release/vs_community.exe
start /w vs_community.exe --passive --wait --norestart --nocache --installPath "%ProgramFiles(x86)%\Microsoft Visual Studio\2019\Community" --add Microsoft.VisualStudio.Component.Windows10SDK.19041 --add Microsoft.VisualStudio.Component.VC.Tools.x86.x64
del /q vs_community.exe
winget install --id Swift.Toolchain
```

These commands download Swift and its dependencies. You’ll see installer windows will pop up along the way; just click through them to complete the installation.

When you’re done, close and reopen **Command Prompt**, and verify that you can run the following command:

```
swift --version
```

## Known issues

- The REPL is currently unavailable on Windows ([#13804](https://bugs.swift.org/browse/SR-13804)).
- Running source files with `swift` is currently unavailable on Windows ([#13805](https://bugs.swift.org/browse/SR-13805)).
- When using **`swiftc`**, you have to add either `-sdk $env:sdkroot` (in **PowerShell**) or `-sdk %sdkroot%` (in **Command Prompt**) to your command.
- Executables ran using `swift run` behave incorrectly ([#13806](https://bugs.swift.org/browse/SR-13806)). As a workaround, use `swift build` to build the package, then run the executable manually.
- Unicode output may not display properly on the command line ([#13807](https://bugs.swift.org/browse/SR-13807)). For the best results, use [Windows Terminal](https://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701) and execute `chcp 65001` prior to running a Swift application that outputs Unicode.

---

Last updated: 23 Oct. 2021 \
Authors: [Saleem Abdulrasool](https://github.com/compnerd), [Steven Van Impe](https://github.com/svanimpe)
