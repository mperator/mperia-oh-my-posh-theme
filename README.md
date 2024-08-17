# Oh-my-posh Setup on Windows

## Overview
This guide shows how to install oh-my-posh and configure it for using in pwsh.exe, Windows Terminal, Visual Studio Code and Visual Studio 2022.

You can find a guide for other OS types on https://ohmyposh.dev/docs/

## Installation
The first step is to install powershell and oh-my-posh from the Microsoft Store.

- https://apps.microsoft.com/detail/9mz1snwt0n5d?hl=en-us&gl=US
- https://apps.microsoft.com/detail/xp8k0hkjfrxgck?hl=en-us&gl=US

We will use CascadiaCode Nerd Font. Therefore we need to download the font from https://www.nerdfonts.com/font-downloads and install it on the computer.
Make sure to install the ttf file. For this setup we will mainly use the font CaskaydiaCoveNerdFontMono-Regular.ttf and DejaVuSansMNerdFontMono-Regular.ttf.

Launch powershell and open the powershell profile in your editor of choice.

``` sh
code $PROFILE
```

Add following line to the profile to initialize powershell on start.

``` ps1
oh-my-posh init pwsh | Invoke-Expression
```

## Configuration

### PowerShell Core
Change the font of the PowerShell to `CaskaydiaCove NFM`.

### Windows Terminal
Change the font of the PowerShell profile to `CaskaydiaCove Nerd Font Mono`.

### Visual Studio Code
Add or change line of VSCode settings: 

``` json
"terminal.integrated.fontFamily": "CaskaydiaCove Nerd Font Mono"
```

### Visual Studio 2022
Change the terminal text font to `DejaVuSans Nerd Font Mono`.

To add PowerShell Core as Terminal copy the default terminal entry and change the Shell Location to the installed path of the Store App. You may need to copy the path into the Shell Location field.

## Oh-my-posh configuration
Add the mperia.omp.json file into the folder where the powershell profile is located. Then update the powershell profile to:

``` ps1
oh-my-posh init pwsh --config '<Your path>\PowerShell\mperia.omp.json' | Invoke-Expression
```

Optionally you can install the posh-git extension following this readme: https://github.com/dahlbyk/posh-git