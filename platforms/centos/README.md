# CentOS

[**CentOS**](https://centos.org) is derived from Red Hat Enterprise Linux (RHEL), without requiring licenses to run. The instructions below will also work for RHEL 8 and later.

First, open the **Terminal** application and run the following command to install the EPEL (Extra Packages for Enterprise Linux) repository:

```
sudo dnf install https://dl.fedoraproject.org/pub/epel/epel-release-latest-8.noarch.rpm
```

> **Note**: This command requires administrator privileges, so it’ll ask for your password.

After the EPEL repository has been added, run the following command to install Swift:

```
sudo dnf install -y swift-lang
```

You can now execute the `swift` command to verify which version you have installed:

```
swift --version
```

---

Last updated: 22 Oct. 2020 \
Author: [Ron Olson](https://github.com/tachoknight)
