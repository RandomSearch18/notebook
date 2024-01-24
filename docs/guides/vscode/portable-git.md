# Using PortableGit with a (portable) VSCode installation

If you have Git installed system-wide, it will be automatically detected by VSCode and you can use its built-in UI to easily access Git features. If you're running programs off of a USB stick or other self-contained folder, you can arhieve the same thing by giving VSCode the path to a PortableGit installation.

## Step 1: Set up PortableGit

If you haven't already set up a PortableGit installation, follow the [Set up PortableGit guide](portable-git.md).

## Step 2: Tell VSCode to use the PortableGit installation

1. Run Visual Studio Code
2. Open the Settings UI (<kbd>Ctrl</kbd>+<kbd>,</kbd>)
3. Search for "git path" to find the **Git: Path** setting
4. Click the "edit in settings.json" link for that setting
5. Provide the path to the `git.exe` file in the `bin` folder of your PortableGit installation, being sure to escape backslashes. It should look like this:
```json
{
    ...
    "git.path": "E:\\Programs\\Git\\bin\\git.exe"
}
```
6. Save the `settings.json` file and reload VSCode (run **Developer: Reload Window** from the command pallete)
7. Open the source control sidebar by clicking on the icon in the activity bar or running **View: Show Source Control** from the command pallete
8. Verify that Git is available by checking the text in the source control sidebar:
    - "No source control providers registered" means that VSCode is still starting up
    - "Scanning folder for Git repositories" means that VSCode is still starting up
    - If you see a "download Git for Windows" button, VSCode has not found your Git installation. Double-check the provided file path.
    - If you see "open folder" and "clone repository" button, Git is installed and avilable to VSCode 🎉
    - If you see a "commit" button, Git is available to VSCode, and you already have a Git repository open 🎉
