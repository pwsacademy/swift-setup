# Ubuntu / Pop!_OS LTS 20.04

[**Ubuntu**](https://ubuntu.com) was the first Linux distribution to support Swift. Unfortunately, Swift isn’t available as a native package yet, so you’ll have to download and install it manually.

[**Pop!_OS**](https://pop.system76.com) is derived from Ubuntu, so the following instructions apply to Pop!_OS as well.

First, open the **Terminal** application and run the following command to install the software Swift depends on:

```
sudo apt-get install \
             binutils \
             git \
             gnupg2 \
             libc6-dev \
             libcurl4 \
             libedit2 \
             libgcc-9-dev \
             libpython2.7 \
             libsqlite3-0 \
             libstdc++-9-dev \
             libxml2 \
             libz3-dev \
             pkg-config \
             tzdata \
             zlib1g-dev
```

> **Note**: This command requires administrator privileges, so it’ll ask for your password.

Next, head over to [swift.org](https://swift.org/download/) and download the latest release of Swift for Ubuntu 20.04. At the time of writing, this release is 5.3 and the file you’ll download is **swift-5.3-RELEASE-ubuntu20.04.tar.gz**. Save this file to your **Downloads** directory.

Back in Terminal, navigate to the **Downloads** directory:

```
cd ~/Downloads
```

The file you downloaded is a compressed archive. Extract it with the following command:

```
tar -xzf swift-5.3-RELEASE-ubuntu20.04.tar.gz
```

> **Note**: Try pressing the **TAB** key after typing the first letters of this filename. Terminal can auto-complete filenames for you. This saves time and avoids mistakes.

The previous command creates a **swift-5.3-RELEASE-ubuntu20.04** directory with the contents of the archive. You can now remove the archive:

```
rm swift-5.3-RELEASE-ubuntu20.04.tar.gz 
```

Although you can use Swift from the **Downloads** directory, it’s better to give it a more suitable home on your system. Use the following command to move Swift into the **/opt** directory:

```
sudo mv swift-5.3-RELEASE-ubuntu20.04 /opt/swift
```

> **Note**: This command requires administrator privileges, so it’ll ask for your password.

Finally, you need to tell Terminal where it can find the **`swift`** command. Open the **.bashrc** configuration file with the **Gedit** text editor:

```
gedit ~/.bashrc
```

At the bottom of this file, add the following line:

```
export PATH=/opt/swift/usr/bin:"${PATH}"
```

Save your changes, exit Gedit, and reload Terminal.

You can now execute the `swift` command to verify which version you have installed:

```
swift --version
```

---

Last updated: 24 Oct. 2020 \
Author: [Steven Van Impe](https://github.com/svanimpe)
