# Install Git using WinGet

## Step 1: Use PowerShell and `winget` to install Git

The `winget` program lets you install some apps onto school computers without admin rights. We will use it to install Git for Windows, making it available for your user on that specific computer.

1. Open a Powershell window (<kbd>Win</kbd>+<kbd>X</kbd> > **Windows PowerShell**)
2. Enter the following command: `winget install -e --id Git.Git --source winget`
3. The Git for Windows will download and be run automatically. This takes a minute or two.
