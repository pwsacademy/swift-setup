# Ubuntu 22.04 LTS

[**Ubuntu**](https://ubuntu.com) was the first Linux distribution to support Swift. Together with [Visual Studio Code](../../editors/vscode-linux/README.md), it makes an excellent development platform for students using Linux.

These instructions rely on the official [**Swiftly**](https://swift-server.github.io/swiftly/) toolchain manager.

Open the **Terminal** application and run the following command to install **swiftly**:

```
curl -L https://swift-server.github.io/swiftly/swiftly-install.sh | bash
```

During installation, select **1** to proceed with the default installation.

After installation, run the following command to make **swiftly** available in your terminal:

```
source .local/share/swiftly/env.sh
```

Alternatively, you can also log out of your current desktop session, then log in again.


Now that **swiftly** is available, install the latest release of Swift with the following command:

```
swiftly install latest
```

Finally, verify that you can run the following command:

```
swift --version
```

---

Last updated: 22 Sept. 2023 \
Author: [Steven Van Impe](https://github.com/svanimpe)
