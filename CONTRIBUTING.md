
# Contributing to ROHD

Thank you for considering contributing to ROHD!  Contributions from the community are vital to making this a successful project.

Anyone interested in participating in ROHD is more than welcome to help!

## Code of Conduct

ROHD adopts the Contributor Covenant v1.4 for the code of conduct.  It can be accessed [here](https://github.com/intel/rohd/blob/main/CODE_OF_CONDUCT.md).

## Getting Help
### Chat on Discord
Discord is a free online instant messaging app which you can use directly in your web browser or install to your device.  Feel free to join to look around at the conversations and have a real-time discussion with the ROHD community.  This a great place to ask questions, get help, engage with the rest of the community, and discuss new ideas.

Join the Discord server here: https://discord.com/invite/jubxF84yGw

### Issues
If something doesn't seem right, you're stuck, there's a critical feature/enhancement missing, you find a bug, etc. then filing an issue on the GitHub repository is a great option.  Please try to provide as much detail as possible.  Complete, stand-alone reproduction instructions are extremely helpful for bugs!

You can file an issue here: https://github.com/intel/rohd/issues/new

### Discussions
GitHub Discussions is a place where you can find announcements, ask questions, share ideas, show new things you're working on, or just discuss in general with the community!  If you have a question or need some help, this is a great place to go.

You can access the discussions area here: https://github.com/intel/rohd/discussions

### StackOverflow
StackOverflow.com is a great tool to ask questions and get answers from the community.  Use the `rohd` tag when asking your question so that others in the community who subscribe to that tag can find and answer your question more quickly!

### Meetings in the ROHD Forum
The [ROHD Forum](https://github.com/intel/rohd/wiki/ROHD-Forum) is a periodic virtual meeting for developers and users of ROHD that anyone can join.  Feel free to join the call!

## Getting Started

### Requirements
You must have [Dart](https://dart.dev/) installed on your system to use ROHD.  You can find detailed instructions for how to install Dart here:
https://dart.dev/get-dart

To run the complete ROHD test suite for development, you need to install [Icarus Verilog](http://iverilog.icarus.com/).  It is used to compare SystemVerilog functionality with the ROHD simulator functionality.  Installation instructions are available here: https://iverilog.fandom.com/wiki/Installation_Guide

### Setup Recommendations
[Visual Studio Code (vscode)](https://code.visualstudio.com/) is a great IDE for development.  You can find installation instructions for vscode here: https://code.visualstudio.com/Download

If you're developing on a remote host, vscode has a Remote SSH extension that can help: https://code.visualstudio.com/blogs/2019/07/25/remote-ssh

If you're on Microsoft Windows, you may want to consider developing with Ubuntu WSL for a Linux environment: https://docs.microsoft.com/en-us/windows/wsl/install-win10

### Cloning and Running the Tests
Once requirements are installed, you can clone and run the test suite.
```
git clone https://github.com/intel/rohd.git
cd rohd
dart run test
```
## How to Contribute
### Reporting Bugs
Please report any bugs you find as a GitHub issue. Please try to provide as much detail as possible. Complete, stand-alone reproduction instructions are extremely helpful for bugs!

Some helpful information you can include:
* Output of `dart --version`
* Your dependencies from pubspec.yaml
* The version of ROHD you're using
* Command you ran and output
* Reproduction code and steps

### Suggesting Enhancements
If you have an idea for a feature or enhancement that would make ROHD better, feel free to submit a GitHub issue!  Discussion on the ticket about pros & cons, strategy, etc. is encouraged.

### Discussing Issues
If you have an opinion or helpful information on any open issue, feel free to comment!  Even if you don't have the time to implement a change, providing valuable input is great too!

### Fix or implement an Issue
Take a look around the issues on the repo and see if there's any you'd like to take ownership of.  For your first contributions, look for issues tagged with `good first issue`, which are intended to be easier to get started with.  Feel free to ask for help or guidance!

### Pull Requests
If you have a change that you have implemented and would like to contribute, you can open a pull request.  Please try to make sure you have implemented tests covering the changes, if applicable.  Smaller, simpler pull requests are easier to review.

Be sure to run the test suite (`dart test`) before asking for your code to be merged.  You may also locally generate API documentation (`dartdoc`) to make sure it looks right and doesn't have any errors.  You should use the dart formatter on all code (`dart format .`), and may prefer to have it automatically format on every file save.  If you're using Visual Studio Code, you could add this to `settings.json`:
```json
"[dart]": {
    "editor.defaultFormatter": "Dart-Code.dart-code",
    "editor.formatOnSave": true,
}
```

**Tests must pass, documentation must generate, and the formatter must be run on every pull request or the automated GitHub Action flow will fail.**

Maintainers of the project and other community members will provide feedback and help iterate as necessary until the contribution is ready to be merged.

Please include the SPDX tag near the top of any new files you create:
```dart
/// SPDX-License-Identifier: BSD-3-Clause
```

You may find that reading the [Architecture](doc/Architecture.md) document will be helpful to becoming familiar with the design of the ROHD framework.

### Creating a New Package
Not every new contribution has to go directly into the ROHD framework!  If you have an idea for a reusable piece of hardware, tooling, verification collateral, or anything else that helps the ROHD ecosystem but is somewhat standalone, you can make your own package that depends on ROHD.  Building an ecosystem of reusable components is important to the success of ROHD.  Reach out if you want some help or guidance deciding if or how you should create a new package.

## Style
ROHD follows the official Dart recommended style guides and lints, and depends on the [lints](https://pub.dev/packages/lints) package.  This package will help ensure that your code is written consistently with the rest of ROHD.

Here are some links to help guide you on style as recommended by Dart:
* Effective Dart: https://dart.dev/guides/language/effective-dart
* Style: https://dart.dev/guides/language/effective-dart/style
* Documentation: https://dart.dev/guides/language/effective-dart/documentation
* Usage: https://dart.dev/guides/language/effective-dart/usage
* Design: https://dart.dev/guides/language/effective-dart/design

We recommend following these same guidelines for any of your own packages you may create for the ecosystem, as well.
