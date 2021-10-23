# CentOS 8<br>Red Hat Enterprise Linux 8

[**CentOS**](https://centos.org) is derived from [**Red Hat Enterprise Linux (RHEL)**](https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux) but doesn’t require a license to run. The instructions below apply to both CentOS and RHEL 8.

First, open the **Terminal** application and run the following command to install the **Extra Packages for Enterprise Linux (EPEL)** repository:

```
sudo dnf install https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm
```

> **Note**: This command requires administrator privileges, so it’ll ask for your password.

Next, install Swift and its dependencies:

```
sudo dnf install -y git swift-lang
```

You can now execute the `swift` command to verify which version you have installed:

```
swift --version
```

## Known issues

- The REPL doesn’t show certain characters and can behave erratically ([#13029](https://bugs.swift.org/browse/SR-13029), [#13885](https://bugs.swift.org/browse/SR-13885?filter=10506)).

---

Last updated: 23 Oct. 2021 \
Authors: [Ron Olson](https://github.com/tachoknight), [Steven Van Impe](https://github.com/svanimpe)
