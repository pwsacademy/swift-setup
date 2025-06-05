# Ubuntu 24.04 LTS

[**Ubuntu**](https://ubuntu.com) was the first Linux distribution to support Swift. Together with [Visual Studio Code](../../editors/vscode-linux/README.md), it makes an excellent development platform for students using Linux.

## Installation

[Swiftly](https://github.com/swiftlang/swiftly) is the recommended way to install Swift on Ubuntu. Execute the following commands in the **Terminal** application to install Swiftly and Swift.

First, make sure that **curl** is installed on your system:

```
sudo apt install -y curl
```

Next, use **curl** to download the Swiftly installer:

```
curl -O https://download.swift.org/swiftly/linux/swiftly-1.0.0-$(uname -m).tar.gz
```

Now unzip the file you just downloaded:

```
tar -zxf swiftly-1.0.0-$(uname -m).tar.gz
```

And run it as follows:

```
./swiftly init
```

This will configure Swiftly and download the latest release of Swift.

Swiftly will list any dependencies that are missing on your system and shows you the command you need to install them. On my system, that command was:

```
sudo apt-get -y install binutils git gnupg2 libcurl4-openssl-dev libgcc-13-dev libpython3-dev libstdc++-13-dev libxml2-dev libncurses-dev libz3-dev pkg-config zlib1g-dev
```

> **⚠️ Warning**: Your system may require a different command. Always use the command printed by Swiftly, not this example.

Swiftly will also show some additional commands needed to complete the installation process. Run these now:

```
source ~/.local/share/swiftly/env.sh
hash -r
```

Finally, run the following command to verify which version of Swift you have installed:

```
swift --version
```

---

Last updated: 4 Jun. 2025 \
Author: [Steven Van Impe](https://github.com/svanimpe)
