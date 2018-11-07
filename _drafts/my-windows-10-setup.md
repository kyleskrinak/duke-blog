---
layout: single
title: My Windows 10 Setup
excerpt: How I like my default Windows 10 configured
header:
  overlay_image: /assets/images/hot_tub.jpg
  overlay_filter: rgba(128, 0, 0, 0.5)
  caption: image from [here](https://commons.wikimedia.org/wiki/File:Bagby_hot_springs_oregon.jpg#file)
categories:
  - lchf
  - Personal productivity
---

## My current Windows 10 configuration

1. TTS default Windows image.

    a. Uses the 32-bit version of Office. I’m unclear why I need the 64-bit version?

1. Taskbar UI changes

    a. Auto-hide taskbar

    a. Small buttons

1. Run Windows Update

1. [Enable the WSL feature](https://docs.microsoft.com/en-us/windows/wsl/install-win10 "Enable the WSL feature")

    a. Paste into PowerShell

    a. `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`

    a. Restart

1. Download Ubuntu from the Microsoft Store

    a. Current LTS is 18.04

1. Enable Hyper-V and Containers in Windows 10

    a. `Enable-WindowsOptionalFeature -Online -FeatureName containers –All`

    a. `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Hyper-V –All`

1. [Install chocolatey](https://chocolatey.org/docs/installation#installing-chocolatey "Install chocolatey") 

    a. Open cmd.exe as admin

    a. `@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"`

    a. Chocolatey installs

      1. My standard apps that aren’t part of the TTS package

          a. `choco install -y docker gimp inkscape vlc babun vim-tux python`

1. Docksal.io

    a. You must use the Babun option. For security reasons, we’ve disabled SMBv1

1. Xenu link sleuth

    a. Download here: http://home.snafu.de/tilman/xenulink.html

1. UI tweaks

    a. Under Settings > Multitasking

      1. Disable “when I resize a snapped window, simultaneously resize any adjacent window.”

      1. Disable “When I snap a window, show what I can snap next to it.” 

1. Install my autoloadahk file to shell:startup

1. Miscellaneous

  a. robocopy backup to D drive

   1. `PS D:\kds38> robocopy C:\Users\kds38 d:\kds38 /MIR /W:1 /R:1 /XJ /NFL /NDL /XD "C:\Users\kds38\OneDrive" "C:\Users\kds38\OneDrive - Duke University" "C:\Users\kds38\AppData`
"
