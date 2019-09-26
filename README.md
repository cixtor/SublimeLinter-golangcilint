# SublimeLinter-golangcilint [![Build Status](https://travis-ci.org/SublimeLinter/SublimeLinter-golangcilint.png?branch=master)](https://travis-ci.org/SublimeLinter/SublimeLinter-golangcilint)

This linter plugin for [SublimeLinter](https://github.com/SublimeLinter) provides an interface to [golangci-lint](https://github.com/golangci/golangci-lint), a linter for Go (golang).

**Note:** The project was originally written by @alecthomas as an alternative to [SublimeLinter-gometalinter](https://github.com/alecthomas/SublimeLinter-contrib-gometalinter), a linter plugin for [gometalinter](https://github.com/alecthomas/gometalinter), both developed by the same person, and [deprecated on Apr 7, 2019](https://github.com/alecthomas/gometalinter/issues/590). The maintenance of the project was passed on to me on [Mar 5, 2019](https://github.com/SublimeLinter/package_control_channel/pull/83#issuecomment-469871377) after I suggested [some improvements](https://github.com/alecthomas/SublimeLinter-contrib-golang-cilint/pull/4) to deal with some false positives in golangci-lint.

## Installation

- Install SublimeLinter 3 from [here](https://packagecontrol.io/packages/SublimeLinter)
- Install SublimeLinter-golangcilint from [here](https://packagecontrol.io/packages/SublimeLinter-golangcilint)
- Install the `golangci-lint` helper from [here](https://github.com/golangci/golangci-lint#install)

![screenshot](screenshot.png)

## Configuration

In order for `golangci-lint` to be executed by SublimeLinter, you must ensure that its path is available to SublimeLinter. Before going any further, please read and follow the steps in [Finding a linter executable](http://sublimelinter.readthedocs.org/en/latest/troubleshooting.html#finding-a-linter-executable) through “Validating your PATH” in the documentation. Once you have installed `golangci-lint`, you can proceed to install the plugin if it is not yet installed.

Due to performance issues in golangci-lint, the linter will not attempt to lint more than one-hundred (100) files considering a delay of 100ms and `lint_mode` equal to “background”. If the user increases the delay, the tool will have more time to scan more files and analyze them. If your project contains more than 300 files, you’ll have to set a delay of 0.3s or more in SublimeLinter settings.

## Plugin installation

Please use [Package Control](https://packagecontrol.io/) to install the linter plugin. This will ensure that the plugin will be updated when new versions are available. If you want to install from source so you can modify the source code, you probably know what you are doing so we won’t cover that here.

To install via Package Control, do the following:

1. Within Sublime Text, “Tools > Command Palette”, then type `install`. Among the commands you should see `Package Control: Install Package`. If that command is not highlighted, use the keyboard or mouse to select it. There will be a pause of a few seconds while Package Control fetches the list of available plugins.
1. When the plugin list appears, type `golangci-lint`. Among the entries you should see `SublimeLinter-golangcilint`. If that entry is not highlighted, use the keyboard or mouse to select it.
