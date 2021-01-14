# Windows

## Apps

Installing apps manually sucks so I prefer to use chocolatey. Below is command that installs my apps

```powershell
choco install jre8 7zip winrar blender gimp vscode openjdk8 openjdk11 golang ruby nvm youtube-dl spotify microsoft-teams git ffmpeg vcredist140 vlc dotnetfx vcredist-all whatsapp vcredist2015 firacode github-desktop geforce-game-ready-driver directx obs-studio chromedriver anaconda3 telegram google-backup-and-sync php yarn procexp microsoft-windows-terminal qbittorrent fiddler docker-desktop winpcap authy-desktop googlechrome androidstudio
```

## WSL2

WSL is amazing it lets you use whole linux potential without creating vm or dualbooting it.

<details>
<summary>Installation</summary>

### Enable Windows Subsystem for Linux

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

### Enable Virtual Machine feature

```powershell
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

### Download the Linux Kernel update package

```powershell
(New-Object System.Net.WebClient).DownloadFile("https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi","$HOME\Downloads\wsl_update_x64.msi")
Start-Process ("$HOME\Downloads\wsl_update_x64.msi")
```

### Set WSL 2 as your default version

```powershell
wsl --set-default-version 2
```

### Install Linux distro

I usually choose [Ubuntu](https://www.microsoft.com/store/apps/9n6svws3rx71) or [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)

</details>

## Config

### Mouse

Mouse acceleration in windows sucks so I just disable it

![mouse settings](https://raw.githubusercontent.com/xNetcat/notes/main/images/mouse-settings.png)
