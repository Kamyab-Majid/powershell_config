# How to setup powershell themes
code $Profile
## Profile

Import-Module posh-git

#region conda initialize
(& "C:\Users\Majid.Kamyab\Anaconda3\Scripts\conda.exe" "shell.powershell" "hook") | Out-String | Invoke-Expression
#endregion

Set-PSReadlineKeyHandler -Key Tab -Function MenuComplete
oh-my-posh --init --shell pwsh --config C:\Users\Majid.Kamyab\Documents\agnoster.omp.json | Invoke-Expression


## Installation commands
```powershell
Install-Module posh-git -Scope CurrentUser -AllowPrerelease -Force

Install-Module posh-git -Scope CurrentUser -Force

Install-Module PowerShellGet -Force -SkipPublisherCheck

Import-Module posh-git

Add-PoshGitToProfile -AllHosts

Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy RemoteSigned -Force

winget install JanDeDobbeleer.OhMyPosh -s winget

winget install --id=Microsoft.WindowsTerminal -e
```

install conda then
```powershell
conda init powershell
```
## Font
install and set terminal font to `DejaVuSansM Nerd Font Propo`



