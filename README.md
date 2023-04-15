# Neals dotfiles

## Contents

-   Optionals
-   Powershell

## Optionals

-   [Nerd Fonts - Hack.zip - Install all of em](https://github.com/ryanoasis/nerd-fonts/releases/tag/v2.3.3)

## Windows Terminal

-   Copy terminal/settings.json to Win Terminal settings

## PowerShell setup (Windows)

-   [Powershell 7](https://learn.microsoft.com/en-us/powershell/scripting/install/installing-powershell-on-windows?view=powershell-7.3) - Better than the default
-   [Scoop](https://scoop.sh/) - A command-line installer
-   [Git for Windows](https://gitforwindows.org/)
-   [Oh My Posh](https://ohmyposh.dev/) - Prompt theme engine
-   [Terminal Icons](https://github.com/devblackops/Terminal-Icons) - Folder and file icons
-   [PSReadLine](https://docs.microsoft.com/en-us/powershell/module/psreadline/) - Cmdlets for customizing the editing environment, used for autocompletion
-   [z](https://www.powershellgallery.com/packages/z) - Directory jumper
-   [PSFzf](https://github.com/kelleyma49/PSFzf) - Fuzzy finder

### Quick Start

Install commands in order of the resources listed above

```pwsh
# Install pwsh 7
winget install --id Microsoft.Powershell --source winget

# Install scoop
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser # Optional: Needed to run a remote script the first time
irm get.scoop.sh | iex

# Install tools
scoop install https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/oh-my-posh.json
scoop bucket add extras
scoop install terminal-icons neovim fzf nvm

Install-Module PSReadLine
Install-Module -Name z
Install-Module -Name PSFzf -Scope CurrentUser -Force
Install-Module -Name posh-git
Install-Module -Name oh-my-posh

# Set Posh theme
Get-PoshThemes
oh-my-posh init pwsh --config "$env:USERPROFILE\AppData\Local\Programs\oh-my-posh\themes\catppuccin.omp.json" | Invoke-Expression

cd $env:USERPROFILE\
mkdir .config/powershell
# Copy user_profile.ps1 from repo\.config\powershell to C:\Users\<yourusername>\.config\powershell

# Update profile to call custom userprofile
echo '. $env:USERPROFILE\.config\powershell\user_profile.ps1' > $PROFILE.CurrentUserCurrentHost
```
