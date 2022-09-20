# Ubuntu 22.04 LTS

[**Ubuntu**](https://ubuntu.com) was the first Linux distribution to support Swift. Together with [Visual Studio Code](../../editors/vscode-linux/README.md), it makes an excellent development platform for students using Linux.

These instructions use packages from the [**Swift Community APT Repository**](https://www.swiftlang.xyz) and may also apply to other releases of Ubuntu, as well as distributions derived from it.

Open the **Terminal** application and run the following commands to install the Swift Community APT Repository:

```
sudo apt install -y curl
curl -s https://archive.swiftlang.xyz/install.sh | sudo bash
```

At the prompt, enter **1** to select the latest stable release of Swift.

Next, install Swift:

```
sudo apt install swiftlang
```

Finally, verify that you can run the following command:

```
swift --version
```

---

Last updated: 20 Sept. 2022 \
Author: [Steven Van Impe](https://github.com/svanimpe)
