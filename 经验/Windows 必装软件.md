# Windows 必装软件

## 网络

### Clash Verge

Windows 端最好用的代理工具，稳如老狗。

```powershell
scoop bucket add extras; scoop install extras/clash-verge-rev
```

## 驱动

### AMD Software: Adrenalin Edition

```powershell
choco install amd-software-adrenalin-edition -y
```

## 系统工具

### 火绒

- 直达链接：<https://www.huorong.cn/product/downloadHr60.php?pro=hr60&plat=x64UrlAll>。

```powershell
$setupFileName="huorong-setup"; curl "https://www.huorong.cn/product/downloadHr60.php?pro=hr60&plat=x64UrlAll" -C - -L -o "$env:TEMP/$setupFileName.exe"; Start-Process -FilePath "$env:TEMP/$setupFileName.exe" -Verb RunAs
```

### Bitwarden

```powershell
scoop install extras/bitwarden
```

### Bandizip

```powershell
scoop install extras/bandizip
```

### Listary

效率工具，快捷启动应用，搜索本地文件（不亚于 Everything 的搜索速度）。

```powershell
scoop install extras/listary
```

### PixPin

截图软件，功能齐全。

```powershell
winget install PixPin.PixPin
```

### Everything

搜索本地文件，极快的搜索速度。

```powershell
scoop install extras/everything
```

### Geek Uninstaller

```powershell
scoop install extras/geekuninstaller
```

### Quicklook

```powershell
scoop install extras/quicklook
```

### ImageGlass

美观，支持格式齐全，开源的图片查看软件。

```powershell
scoop install extras/quicklook
```

### Notepad3

简洁，美观的文本编辑软件。

```powershell
scoop install extras/notepad3
```

### PotPlayer

史上最强视频播放软件。

```powershell
scoop install extras/potplayer
```

### SumatraPDF

轻量的 PDF 阅读软件。

```powershell
scoop install extras/sumatrapdf
```

### Readest

现代化的电子书阅读器，支持多种电子书格式，提供舒适的阅读体验。

```powershell
scoop install extras/readest
```

### Motrix

```powershell
scoop install extras/motrix
```

### qBittorrent Enhanced Edition

开源的 BT 下载器 qBittorrent 的增强版。

```powershell
scoop install extras/qbittorrent-enhanced
```

### 微信输入法

```powershell
winget install Tencent.WeType
```

## 娱乐

### Mozilla Firefox

黑客用的 Web 浏览器！

```powershell
scoop install extras/firefox
```

### Google Chrome

最有脸面的 Web 浏览器。

```powershell
scoop install extras/googlechrome
```

### QQ

功能丰富的通讯软件。

```powershell
scoop install extras/qq-nt
```

### 微信

简单的通讯软件。

```powershell
scoop install extras/wechat
```

### Steam

电子游戏平台。

```powershell
scoop install games/steam
```

### 酷狗音乐

超前的音乐软件。

- 官网：<https://download.kugou.com/>
- 直达链接：<https://download.kugou.com/dl/kugou_pc>

```powershell
$setupFileName="kugou-setup"; curl "https://download.kugou.com/dl/kugou_pc" -C - -L -o "$env:TEMP/$setupFileName.exe"; Start-Process -FilePath "$env:TEMP/$setupFileName.exe" -Verb RunAs
```

## 办公

### Xmind

最好的思维导图软件。

```powershell
scoop install extras/xmind
```

### Typora

最稳定的 Markdown 编辑软件。

```powershell
scoop install extras/typora
```

### LibreOffice

```powershell
scoop install extras/libreoffice
```

## 开发工具

### VirtualBox

```powershell
scoop install nonportable/virtualbox-with-extension-pack-np
```

### Powershell

```powershell
scoop install main/pwsh
```

### VSCode

```powershell
scoop install extras/vscode
```

### GCC

```powershell
scoop install main/gcc
```

### Qt

开源，跨平台，功能丰富强大的 C++ 软件开发框架。

- 下载链接：<https://download.qt.io/official_releases/online_installers/qt-online-installer-windows-x64-online.exe>

```powershell
$setupFileName="qt-setup"; curl "https://download.qt.io/official_releases/online_installers/qt-online-installer-windows-x64-online.exe" -C - -L -o "$env:TEMP/$setupFileName.exe"; Start-Process -FilePath "$env:TEMP/$setupFileName.exe" -Verb RunAs
```

### pnpm

[pnpm](https://pnpm.io/)：一款快速且节省磁盘空间的 Node 包管理器。

```powershell
scoop install main/pnpm
```

### Node.js

作为一个异步事件驱动的 JavaScript 运行库，[Node.js](https://nodejs.org/) 旨在构建可扩展的网络应用程序。

```powershell
scoop install main/nodejs-lts
```

### Git

[Git](https://git-scm.com/) 是一个[免费且开源](https://git-scm.cn/about/#free-and-open-source)的分布式版本控制系统，旨在快速高效地处理从小型到非常大型的项目。

```powershell
scoop install main/git
```

## CMake

[CMake](https://cmake.org/)：一套用于构建、测试和打包软件的工具家族。

```
scoop install main/cmake
```

### Make

```powershell
scoop install main/make
```

### Python

一种编程语言，助您高效工作并更有效地集成系统。

```powershell
scoop install main/python
```

## 其他

### FreeFileSync

文件同步工具。

```powershell
$html = curl -s https://freefilesync.org/download.php; $downloadLink = $html | Select-String -Pattern 'href="(\/download\/FreeFileSync_[\d\.]+_Windows_Setup\.exe)"' | ForEach-Object { $_.Matches.Groups[1].Value }; $downloadLink = "https://freefilesync.org" + $downloadLink; Write-Host "Downlod Link: $downloadLink";$setupFileName="freefilesync-setup"; curl $downloadLink -C - -L -o "$env:TEMP/$setupFileName.exe"; Start-Process -FilePath "$env:TEMP/$setupFileName.exe" -Verb RunAs
```

### Caesium Image Compressor

批量图片压缩。

```powershell
scoop install extras/caesium-image-compressor
```

### FFmpeg

音视频文件处理工具。

```powershell
scoop install main/ffmpeg
```

### ImageMagick

图片文件处理工具。

```powershell
scoop install main/imagemagick
```

### LocalSend

局域网传输文件。

```powershell
scoop install extras/localsend
```

### OBS Studio

专业，开源的录屏工具。

```powershell
scoop install extras/obs-studio
```

### scrcpy

开源，轻量的手机投屏工具。

```powershell
scoop install main/scrcpy
```

### Upscayl

图片无损放大工具。

```powershell
scoop install extras/upscayl
```

### Keyviz

键盘可视化工具。

```powershell
scoop install extras/keyviz
```

### MacType

Windows 字体渲染效果增强工具。

```powershell
scoop install nonportable/mactype-np
```

### fastfetch

轻量级的系统信息检测工具，能够快速显示系统硬件配置、操作系统信息等。

```powershell
scoop install main/fastfetch
```

## 字体

### Maple-Mono-NF-CN

```powershell
scoop install nerd-fonts/Maple-Mono-NF-CN
```

### Resource Han Rounded CN

```powershell
$html = curl -s -L "https://github.com/CyanoHao/Resource-Han-Rounded/releases/latest"; $version = $html | Select-String -Pattern '<h1 data-view-component="true" class="d-inline mr-3">Resource Han Rounded ([\d\.]+)</h1>' |  ForEach-Object { $_.Matches.Groups[1].Value }; Write-Host "Latest version: $version"; $downloadLink = "https://github.com/CyanoHao/Resource-Han-Rounded/releases/download/v$version/RHR-CN-$version.7z"; Write-Host "Download Link: $downloadLink"; $fontZipName = "resource-han-rounded-cn"; curl $downloadLink -C - -L -o "$env:TEMP/$fontZipName.7z"; 7z x "$env:TEMP/$fontZipName.7z" -o"$env:TEMP/$fontZipName"; $destDir = "C:\Windows\Fonts"; Get-ChildItem -Path "$env:TEMP/$fontZipName" -Recurse -Filter "*.ttf" | ForEach-Object { $destPath = Join-Path -Path $destDir -ChildPath $_.Name; Copy-Item -Path $_.FullName -Destination $destPath -Force; Write-Host "copy: $($_.Name)" }
```



