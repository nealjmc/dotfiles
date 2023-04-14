# Neals dotfiles

## Contents

-   Pre-reqs
-   Powershell

## Pre Reqs

-   [Nerd Fonts - Hack.zip - All of em](https://github.com/ryanoasis/nerd-fonts/releases/tag/v2.3.3)

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
winget install --id Microsoft.Powershell --source winget

Set-ExecutionPolicy RemoteSigned -Scope CurrentUser # Optional: Needed to run a remote script the first time
irm get.scoop.sh | iex

scoop install https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/oh-my-posh.json
scoop bucket add extras
scoop install terminal-icons
Install-Module PSReadLine
Install-Module -Name z
Install-Module -Name PSFzf

```
