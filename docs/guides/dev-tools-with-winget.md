# Installing development tools with WinGet

<!-- > OneDrive is out, local installs are in -->

> OneDrive is so 2024
>
> &mdash; Mish 2024

👉 **[Skip to the guide](#guide)**

## Introduction

WinGet is a package manager that lets you install a selection of apps locally on your current computer. Consider it as a tool to automatically download and run non-elevated installers, or as a more reliable alternative to the Microsoft Store.

Installing programs locally is especially useful when you'll be using the same computer often, as it takes a bit of time to set up, but is currently the best way to use tools like VSCode on school computers. In my opinion, it provides a superior experience to GitHub Codespaces, and doesn't suffer from the bugginess of VSCode installed to OneDrive.

### Notes

After installing a command-line program, ensure you open a new PowerShell window, so that the updates to your `PATH` environment variable are picked up. Logging out and back in again will also do the trick.

WinGet will throw a certificate error on the school network by default, but this can be worked around by adding the `--source winget` argument to any `winget install` command, as in the examples below.

WinGet will usually download the non-privileged installer by default, but if it doesn't then you can use the `--scope user` argument to force it.

### Advantages of installing with WinGet

- Automatically does as much OS integration as possible, e.g. adding executables to PATH, registering as a file handler
- TODO: Add more

### Disadvantages of installing with WinGet

- Programs have to be installed (and configured) separately for every computer that you want to use.
- Not all programs are available on WinGet (although lots are!)

## Guide

You use Winget through its command-line interface. Start by opening a PowerShell window by pressing <kbd>Win</kbd>+<kbd>X</kbd> > **Windows PowerShell**, and then paste your chosen commands in.

### Install VSCode locally

```ps1
winget install -e --id Microsoft.VisualStudioCode --source winget
```

Alternatively, you can install the Insiders version of VSCode:

```ps1
winget install -e --id Microsoft.VisualStudioCode.Insiders --source winget
```

Run it by opening a _new_ PowerShell window, and running the command below

```ps1
code
```

### Install Git locally

```ps1
winget install -e --id Git.Git --source winget
```

## Find other programs to install with WinGet

<https://winget.run/> is a useful website for discovering WinGet packages. Its search is a bit naff, but you can use Google with `site:winget.run` as an alternative, or just include "winget" as a keyword in your Google search.
