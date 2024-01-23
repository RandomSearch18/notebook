# Using PortableGit with a (portable) VSCode installation

[Git](https://git-scm.com/) is a popular version control program, and VSCode has a built-in UI to easily use Git while you're programming. And of course, Git is the software behind Github,
which provides a central platform for storing and sharing Git repositories. PortableGit is a distribution of Git that can run self-contained on a thumb drive (or any other storage device), making it usable on school computers.

If you have Git installed system-wide, it will be automatically detected by VSCode, but this isn't the case for a PortableGit installation. However, setting it up manually only takes a few steps.

## Step 1: Download the PortableGit installer and install it onto your thumb drive

1) Visit the [Git downloads page for Windows](https://git-scm.com/download/win) and download **64-bit Git for Windows Portable**
    - As the installer is a `.exe` file, you won't be able to save it to your home folder
2) Run the installer and provide it with the path to a folder on your thumb drive, e.g. `E:\Programs\Git`
3) The installer will spend some time extracting the files, and then automatically exit as soon as it's done

## Step 2: Tell VSCode to use the PortableGit installation

1) Run Visual Studio Code
2) Open the Settings UI (<kbd>Ctrl</kbd>+<kbd>,</kbd>)
3) Search for "git path" to find the **Git: Path** setting
4) Click the "edit in settings.json" link for that setting
5) Provide the path to the `git.exe` file in the `bin` folder of your PortableGit installation, being sure to escape backslashes. It should look like this:
```json
{
    ...
    "git.path": "E:\\Programs\\Git\\bin\\git.exe"
}
```
6) Save the `settings.json` file and reload VSCode (run **Developer: Reload Window** from the command pallete)
7) Open the source control sidebar by clicking on the icon in the activity bar or running **View: Show Source Control** from the command pallete
8) Verify that Git is available by checking the text in the source control sidebar:
    * "No source control providers registered" means that VSCode is still starting up
    * "Scanning folder for Git repositories" means that VSCode is still starting up
    * If you see a "download Git for Windows" button, VSCode has not found your Git installation. Double-check the provided file path.
    * If you see "open folder" and "clone repository" button, Git is installed and avilable to VSCode 🎉
    * If you see a "commit" button, Git is available to VSCode, and you already have a Git repository open 🎉
