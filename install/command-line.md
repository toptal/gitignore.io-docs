---
description: >-
  To run gitignore.io from your command line you need an active internet
  connection and an environment function. You need to add a function to your
  environment that lets you access the gitignore.io API.
---

# Command Line

### Git

#### Bash <a id="git-bash"></a>

```bash
git config --global alias.ignore \
'!gi() { curl -sL https://www.gitignore.io/api/$@ ;}; gi'
```

### Linux

#### Bash <a id="linux-bash"></a>

```bash
echo "function gi() { curl -sL https://www.gitignore.io/api/\$@ ;}" >> \
~/.bashrc && source ~/.bashrc
```

#### Zsh <a id="linux-zsh"></a>

```bash
echo "function gi() { curl -sLw "\n" https://www.gitignore.io/api/\$@ ;}" >> \
~/.zshrc && source ~/.zshrc
```

#### Fish <a id="linux-fish"></a>

```bash
printf "function gi\n\tcurl -sL https://www.gitignore.io/api/\$argv\nend\n" > \
~/.config/fish/functions/gi.fish
```

### macOS

#### Bash <a id="macos-bash"></a>

```bash
echo "function gi() { curl -sL https://www.gitignore.io/api/\$@ ;}" >> \
~/.bash_profile && source ~/.bash_profile
```

#### Zsh <a id="masos-zsh"></a>

```bash
echo "function gi() { curl -sLw "\n" https://www.gitignore.io/api/\$@ ;}" >> \
~/.zshrc && source ~/.zshrc
```

#### Fish <a id="macos-fish"></a>

```bash
printf "function gi\n\tcurl -sL https://www.gitignore.io/api/\$argv\nend\n" > \
~/.config/fish/functions/gi.fish
```

### Windows

#### PowerShell v3 Script

```bash
#For PowerShell v3
Function gig {
  param(
    [Parameter(Mandatory=$true)]
    [string[]]$list
  )
  $params = ($list | ForEach-Object { [uri]::EscapeDataString($_) }) -join ","
  Invoke-WebRequest -Uri "https://www.gitignore.io/api/$params" | select -ExpandProperty content | Out-File -FilePath $(Join-Path -path $pwd -ChildPath ".gitignore") -Encoding ascii
}
```

#### PowerShell v2 Script <a id="windows-powershell-v2"></a>

```bash
#For PowerShell v2
Function gig {
  param(
    [Parameter(Mandatory=$true)]
    [string[]]$list
  )
  $params = ($list | ForEach-Object { [uri]::EscapeDataString($_) }) -join ","
  $wc = New-Object System.Net.WebClient
  $wc.Headers["User-Agent"] = "PowerShell/" + $PSVersionTable["PSVersion"].ToString()
  $wc.DownloadFile("https://www.gitignore.io/api/$params", "$PWD\.gitignore")
}
```

Create a Command Line Prompt Script If you have installed [msysgit](http://msysgit.github.io/)\), create `gi.cmd` with content below. And copy it to `C:\Program Files\Git\cmd\gi.cmd`, assuming `msysgit` was installed to `c:\Program Files\Git`. Make sure that `C:\Program Files\Git\cmd` is added to the environment variable `path`.

```bash
@rem Do not use "echo off" to not affect any child calls.
@setlocal

@rem Get the abolute path to the parent directory, which is assumed to be the
@rem Git installation root.
@for /F "delims=" %%I in ("%~dp0..") do @set git_install_root=%%~fI
@for /F "delims=" %%I in ("%~dp0..") do @set git_mingw_root=%%~fI\mingw
@if not exist "%git_mingw_root%" @set git_mingw_root=%git_install_root%\mingw64
@set PATH=%git_install_root%\bin;%git_mingw_root%\bin;%PATH%

@if not exist "%HOME%" @set HOME=%HOMEDRIVE%%HOMEPATH%
@if not exist "%HOME%" @set HOME=%USERPROFILE%

@curl.exe -L -s https://www.gitignore.io/api/%*
```

