# How to setup powershell themes
```powershell
code $Profile
```
## Profile
content of profile:
```powershell
Import-Module posh-git

#region conda initialize
(& "C:\Users\Majid.Kamyab\Anaconda3\Scripts\conda.exe" "shell.powershell" "hook") | Out-String | Invoke-Expression
#endregion

Set-PSReadlineKeyHandler -Key Tab -Function MenuComplete
oh-my-posh --init --shell pwsh --config C:\Users\Majid.Kamyab\Documents\agnoster.omp.json | Invoke-Expression
```

## Installation commands
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
install and set terminal font to `DejaVuSansM Nerd Font Propo`
[DejaVuSansM Nerd Font Mono]([https://github.com/cekrem/dotfiles/blob/master/fonts/Meslo%20LG%20L%20DZ%20Regular%20Nerd%20Font%20Complete%20Mono.otf](https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.2/DejaVuSansMono.zip)https://github.com/ryanoasis/nerd-fonts/releases/download/v3.0.2/DejaVuSansMono.zip)


