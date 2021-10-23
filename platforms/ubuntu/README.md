# Ubuntu 21.10<br>Pop!_OS 21.10

[**Ubuntu**](https://ubuntu.com) was the first Linux distribution to support Swift. [**Pop!_OS**](https://pop.system76.com) is derived from Ubuntu, so the following instructions apply to Pop!_OS as well.

Open the **Terminal** application and run the following commands:

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

## Known issues

- The REPL doesn’t show certain characters and can behave erratically ([#13029](https://bugs.swift.org/browse/SR-13029), [#13885](https://bugs.swift.org/browse/SR-13885)).

---

Last updated: 23 Oct. 2021 \
Author: [Steven Van Impe](https://github.com/svanimpe)
