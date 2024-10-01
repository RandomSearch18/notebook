# Installing development tools with WinGet

<!-- > OneDrive is out, local installs are in -->

> OneDrive is so 2024
>
> &mdash; Mish 2024

## Introduction

WinGet is a package manager that lets you install a selection of apps locally on your current computer. Consider it as a tool to automatically download and run non-elevated installers, or as a more reliable alternative to the Microsoft Store.

Installing programs locally is especially useful when you'll be using the same computer often, as it takes a bit of time to set up, but is currently the best way to use tools like VSCode on school computers. In my opinion, it provides a superior experience to GitHub Codespaces, and doesn't suffer from the bugginess of VSCode installed to OneDrive.

### Notes

After installing a command-line program, ensure you open a new PowerShell window, so that the updates to your `PATH` environment variable are picked up. Logging out and back in again will also do the trick.

WinGet will throw a certificate error on the school network by default, but this can be worked around by adding the `--source winget` argument to any `winget install` command, as in the examples below.

### Advantages of installing with WinGet

- OS integration as standard, e.g. adding to PATH, registering as a file handler, etc.
- TODO: Add more

### Disadvantages

- Programs have to be installed (and configured) for every computer that you want to use.

## Guide

You use Winget through its command-line interface. Start by opening a PowerShell window by pressing <kbd>Win</kbd>+<kbd>X</kbd> > **Windows PowerShell**, and then paste your chosen commands in.

### Install VSCode locally

```ps1
winget install -e --id Microsoft.VisualStudioCode --source winget
```

Run it by opening a _new_ PowerShell window, and running the command below

```ps1
code
```

### Install Git locally

```ps1
winget install -e --id Git.Git --source winget
```
