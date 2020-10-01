# Setting up fresh Windows machine
These are my own notes for setting up a new Windows machine. The suite of tools will not suit everyone, but the general procedure serves well as a reference.

## Part I. Chocolatey
> Recommended to use CMD whenever possible. Powershell raises too many security warnings
1. Launch CMD with Administrator privileges.
2. Follow chocolatey installation instructions at https://chocolatey.org/install
3. Re-launch CMD with Administrator privileges.
4. Install the installation utility with 
    ```
    choco install -y instchoco
    ```
5. Restore your packages with 
    ```
    instchoco -y -s <github packages.config URL>
    ```

## (Optional) Restore configs/preferences of individual apps
(To-do)

## Part II. Enable WSL and OpenSSH server
1. In control panel, check *Windows Subsystem for Linux*
2. Restart machine.
3. From *Microsoft Store*, install the following apps
    + Ubuntu 18.04 (because 20.04+ are still not widely supported)
    + Windows Terminal

4. Follow instructions at to enable OpenSSH server

## Part III. Manually installing other apps
- Freemeter - https://www.tiler.com/freemeter/
- Fences (from Steam)
- MS Teams - https://teams.microsoft.com/

## Part IV. Backup choco packages
Unfortunately, only packages from Part I can be backed up and transferred conveniently this way. Other parts will require manual installation.

1. Launch CMD with Administrator privileges.
2. Backup your list of installed apps with 
    ```
    choco-package-list-backup
    ```
3. Backup your files located within `C:\Users\<your-username>\Documents\ChocolateyPackageListBackup` to a secure location such as your cloud storage or GitHub.