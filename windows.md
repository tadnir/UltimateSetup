# Windows

## MicrosoftStore Installations
```
VisualStudio Code
Microsoft PowerToys
Nvidia Control Panel
```


## Font
Get the fonts from [NerdFonts](https://www.nerdfonts.com/), recommended:
* CaskaydiaCove NF

> **_NOTE:_** You should set the font in the terminal app and in any app that emulates a terminal (VSCode/JetBrainsIDEs)


## PowerShell Profile Folder
Run:
```
New-Item -Path $PROFILE -Type File -Force
New-Item -Path "$env:USERPROFILE\.config\powershell\main.ps1" -Type File -Force
notepad $PROFILE
```

Write in the file:
```
. "$env:USERPROFILE\.config\powershell\main.ps1"
```

> From here on use the `main.ps1` file as your profile file (you can `.` include other files from there)


## WinGet Installations
```
winget install powershell -s winget
winget install Google.Chrome -s winget
winget install Google.GoogleDrive -s winget
winget install Git.Git -s winget
winget install GitHub.Cli -s winget
```


## Prompt
### Oh-My-Posh
Get the up-to-date instructions - https://ohmyposh.dev/
```
winget install JanDeDobbeleer.OhMyPosh -s winget
```

Add the following to the end of the powershell profile:
```
oh-my-posh init pwsh --config "$env:POSH_THEMES_PATH/<theme name>.omp.json" | Invoke-Expression
```

Choose the theme with the `Get-PoshThemes` command, recommendations:
* night-wol

> **Dont Modify the files in the themes directory. Create new or modified themes only in a new directory outside OMP**


## Scoop Installation
Get the installation from here - https://scoop.sh/
```
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression
```


## Python
Install [python](https://www.python.org/) and [pipx](https://pipx.pypa.io/stable/installation/#:~:text=your%20installation.-,On%20Windows%3A,-Install%20via%20Scoop)
```
scoop install python
scoop install pipx
pipx ensurepath
```

### Python packages
```
pipx install frogmouth
```
* https://github.com/Textualize/frogmouth


## Zoxide
>Get the full instructions - https://github.com/ajeetdsouza/zoxide?tab=readme-ov-file#installation

Run:
```
scoop install zoxide
scoop install fzf
```
Add the following to the end of the `profile` file:
```
Invoke-Expression (& { (zoxide init powershell | Out-String) })
```


## PowerShell Gallery
Recommendations:
* [Terminal-Icons](https://github.com/devblackops/Terminal-Icons)
```
Install-Module -Name Terminal-Icons -Repository PSGallery
Import-Module Terminal-Icons
```
* [PSReadLine]()
```
Install-Module -Name PSReadLine -Repository PSGallery
Import-Module PSReadLine
```

## WSL
```
????
```


## Others
* [MobaXTerm](https://mobaxterm.mobatek.net/) - `winget instsall Mobatek.MobaXterm -s winget`
* [JetBrains ToolBox](https://www.jetbrains.com/toolbox-app/) - `winget install JetBrains.Toolbox -s winget`

