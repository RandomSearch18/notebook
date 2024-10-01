# Installing development tools with WinGet

<!-- > OneDrive is out, local installs are in -->

> OneDrive is so 2024
> &mdash; Mish 2024

## Introduction

WinGet is a package manager that lets you install a selection of apps locally on your current computer. You can think of it as a tool to automatically download and run non-elevated installers.

### Advantages of installing with WinGet

- OS integration as standard, e.g. adding to PATH, registering as a file handler, etc.
- TODO: Add more

## Steps

```ps1
winget install -e --id Microsoft.VisualStudioCode --source winget
```

```ps1
winget install -e --id Git.Git --source winget
```
