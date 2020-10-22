# Windows

Windows support is still under development.  The latest development snapshots are recommended, though they may be less stable as they are development sanpshots.

## Installation

Download the latest development snapshot from [swift.org](https://swift.org/download).

In order to make the setup easier, download `swift-devenv` from [compnerd/swift-devenv](https://github.com/compnerd/swift-devenv/releases).  Simply copy the `swift-devenv.exe` into the installed toolchain (`%SystemDrive%\Library\Developer\Toolchains\unknown-Asserts-development.xctoolchain\usr\bin`) using Windows Explorer.

In order to build applications for Windows, the Windows SDK must be installed.  You can download the install for the Windows SDK from [Microsoft](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk/).



## Setup

After installation, you will need to perform a preliminary setup that needs to be repeated every time you install a new toolchain or update the Windows SDK.

From the **Command Prompt** run the following command:

```cmd
> swift devenv --deploy
```

Because this copies files into locations that you may not have permissions to write to, it may provide a UAC prompt.  Allow the process to write the files into location.

## Using Swift

In order to be able to build with swift, you need to setup your development environment.  With the `swift-devenv` tool was installed previously, this is a setup command that will need to be run each time the **Command Prompt** is launched.

```cmd
> swift devenv
```

---

Last updated: 21 Oct. 2020 \
Author: [Saleem Abdulrasool](https://github.com/compnerd)
