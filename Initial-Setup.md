* Create account (eg vrjammer) at Github. Account join new (or existing) team/organization called "team-pf" on Github.

* Create account (eg vrjammer) at Unity3d. Download and install Unity3D client. 
The Client comes with an install of Visual Studio 2017 Community edition. Or you can install it separately.

* Create Visual Studio account (eg vrjammer) at Microsoft/MSDN. Download and install Visual Studio Community 2017. 
Choose pre-made Options Unity/Gamedev/Desktop C++.

* go to https://git-scm.com/download/win to install Git for Windows.

## Posh Git

Better integration of *Git* into *Power Shell*

First some scripts require the policy to allow them to execute (RemoteSigned) :
```
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
```
Then you can install posh git from the PowerShell gallery:
```
PowerShellGet\Install-Module posh-git -Scope CurrentUser
```
Import the posh-git script for the current session
```
Import-Module posh-git
```
Then make sure that the extensions are loaded with every instance of the PowerShell, instead of having to import every time:
```
Add-PoshGitToProfile
```
See Posh-Git main page and additional instructions

## Git for Windows

We'll want to connect Github to Git for Windows.

First verify if you already have a SSH key on your local Git for Windows. Open the "Git-Bash" tool and 
```
ls -al ~/.ssh
```
If it returns empty, you have to generate a key :
```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
After generation copy the new SSH key to the clipboard :
```
clip < ~/.ssh/id_rsa.pub
```
then go to your profile settings to add the key

![personal settings](https://help.github.com/assets/images/help/settings/userbar-account-settings.png)

![ssh keys](https://help.github.com/assets/images/help/settings/settings-sidebar-ssh-keys.png)

![add ssh key](https://help.github.com/assets/images/help/settings/ssh-add-ssh-key.png)

![key paste](https://help.github.com/assets/images/help/settings/ssh-key-paste.png)

![add key](https://help.github.com/assets/images/help/settings/ssh-add-key.png)

## This repository

![Visual Studio Clone](Team-Explorer-Clone-This-Repository.png)

