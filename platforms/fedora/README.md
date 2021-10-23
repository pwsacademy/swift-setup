# Fedora 34

[**Fedora**](https://getfedora.org) isn’t officially supported yet, but it has excellent support for Swift and even provides a native package for easy installation.

To install Swift on Fedora, open the **Terminal** program and run the following command:

```
sudo dnf install -y swift-lang
```

> **Note**: This command requires administrator privileges, so it’ll ask for your password.

You can now execute the `swift` command to verify which version you have installed:

```
swift --version
```

## Known issues

- The REPL doesn’t show certain characters and can behave erratically ([#13029](https://bugs.swift.org/browse/SR-13029), [#13885](https://bugs.swift.org/browse/SR-13885)).

---

Last updated: 23 Oct. 2021 \
Authors: [Ron Olson](https://github.com/tachoknight), [Steven Van Impe](https://github.com/svanimpe)
