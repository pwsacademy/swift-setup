# Contributing to Swift Setup

Our instructions are designed to supplement either an introductory programming course in higher education or an advanced programming course in secondary education. Our target audience consists of students taking these courses, and the instructors teaching them.

With that in mind, please adhere to the following guidelines when contributing instructions.

## General

* Target your instructions at novice students. Only assume basic skills — such as file management and web browsing — but nothing more. In particular, don’t assume the student has prior programming experience, or experience with using a command line interface.
* When your instructions involve a graphical user interface, include a screenshot of the interface to clarify the instructions.
* When referring to actions in a graphical user interface, favor menu commands over keyboard shortcuts. It’s much easier for a student to explore a menu and discover a command, than it is to memorize a keyboard shortcut.
* When your instructions use a command line interface, make sure the commands are explicit and reproducible. Assume the student will copy-and-paste the commands and that they won’t be able to compensate for missing commands (such as using `cd` to navigate between directories).
* Add a footer that includes the date, your name, and a link to your GitHub profile so we can contact you in case your instructions need updating.

## Platforms

* To be included in this repository, a platform must have a recent, stable, binary release. Don’t rely on daily builds or building from source code.
* Base your instructions on a fresh install of the platform and provide installation instructions for required software that is not included with the platform.
* End your instructions by running `swift --version` to verify that `swift` is installed and available on the `PATH`.

## Editors and IDEs

* Use the existing instructions as templates.
* The **Features** section serves to compare the different editors and IDEs, so include this section and use it as a checklist.
* Focus your instructions on the specifics of installing and using the editor or IDE. Assume the course you’re supplementing already explains how to use Swift and the Swift Package Manager; this is not something you should get into.
* For cross-platform editors and IDEs, you may cover multiple platforms in a single document, but only if the differences between these platforms are minimal. If not, create a separate document for each platform.
