# How to setup powershell themes
```powershell
code $Profile
```
put the content of the profile.ps1 in that file


## Installation commands
Install anaconda and git if you want.
in order to make conda usable in powerhsell run:
```
conda init powershell
```
in anaconda prompt. 
then run the following commands in powershell.

```powershell
winget install JanDeDobbeleer.OhMyPosh -s winget
Install-Module posh-git -Scope CurrentUser -Force
Install-Module PowerShellGet -Force -SkipPublisherCheck -Scope CurrentUser
Install-Module -Name Terminal-Icons -Repository PSGallery
Install-Module -Name PSReadLine -Scope CurrentUser -Force -SkipPublisherCheck
Import-Module posh-git

Install-Module syntax-highlighting
Add-PoshGitToProfile -AllHosts
Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy RemoteSigned -Force
winget install --id=Microsoft.WindowsTerminal -e
```

install conda then
```powershell
conda init powershell
```
## Font
install and set terminal font to 
(MesloLGLDZ Nerd Font Mono)[https://github.com/cekrem/dotfiles/blob/master/fonts/Meslo%20LG%20L%20DZ%20Regular%20Nerd%20Font%20Complete%20Mono.otf]
