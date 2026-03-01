# Windows 必装软件

## 驱动

### AMD Software: Adrenalin Edition

```powershell
$html = curl -A "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36" -s "https://www.amd.com/zh-cn/support/download/drivers.html"; $downloadLink = $html | Select-String -Pattern 'href="(https:\/\/drivers.amd.com\/drivers\/installer\/[\d.]+\/whql\/amd-software-adrenalin-edition-[\d.]+-minimalsetup-[\d]+_web.exe)"' | ForEach-Object { $_.Matches.Groups[1].Value }; Write-Host "Downlod Link: $downloadLink"; $setupFileName="amd-software-adrenalin-edition-setup"; curl $downloadLink -A "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36" -C - -L -o "$env:TEMP/$setupFileName.exe"; Start-Process -FilePath "$env:TEMP/$setupFileName.exe" -Verb RunAs
```

| `download`      | `dynamic_link`                                               |
| --------------- | ------------------------------------------------------------ |
| `dynamic_link`  | <https://www.amd.com/zh-cn/support/download/drivers.html>    |
| `regex`         | `href="(https:\/\/drivers.amd.com\/drivers\/installer\/[\d\.]+\/whql\/amd-software-adrenalin-edition-[\d\.]+-minimalsetup-[\d]+_web\.exe)"` |
| `download_link` | `regex`                                                      |

## 系统工具

### 火绒

- 直达链接：<https://www.huorong.cn/product/downloadHr60.php?pro=hr60&plat=x64UrlAll>。

```powershell
$setupFileName="huorong-setup"; curl "https://www.huorong.cn/product/downloadHr60.php?pro=hr60&plat=x64UrlAll" -C - -L -o "$env:TEMP/$setupFileName.exe"; Start-Process -FilePath "$env:TEMP/$setupFileName.exe" -Verb RunAs
```

| `download`    | `direct_link`                                                             |
| ------------- | ------------------------------------------------------------------------- |
| `direct_link` | <https://www.huorong.cn/product/downloadHr60.php?pro=hr60&plat=x64UrlAll> |

### 微信输入法

```powershell
winget install Tencent.WeType
scoop install abgox_abyss/Tencent.WeType
```

| `install`     | `scoop`                          |
| ------------- | -------------------------------- |
| `scoop`       | `Tencent.WeType`                 |
| `bucket`      | `abgox_abyss`                    |
| `bucket_link` | <https://github.com/abgox/abyss> |

### Bitwarden

```powershell
scoop install extras/bitwarden
```

| `install` | `scoop`     |
| --------- | ----------- |
| `scoop`   | `bitwarden` |
| `bucket`  | `extras`    |

### Bandizip

```powershell
scoop install extras/bandizip
```

| `install` | `scoop`    |
| --------- | ---------- |
| `scoop`   | `bandizip` |
| `bucket`  | `extras`   |

### Listary

效率工具，快捷启动应用，搜索本地文件（不亚于 Everything 的搜索速度）。

```powershell
scoop install extras/listary
```

| `install` | `scoop`   |
| --------- | --------- |
| `scoop`   | `listary` |
| `bucket`  | `extras`  |

### ImageGlass

美观，支持格式齐全，开源的图片查看软件。

```powershell
scoop install extras/imageglass
```

| `install` | `scoop`      |
| --------- | ------------ |
| `scoop`   | `imageglass` |
| `bucket`  | `extras`     |

### PotPlayer

史上最强视频播放软件。

```powershell
scoop install extras/potplayer
```

| `install` | `scoop`     |
| --------- | ----------- |
| `scoop`   | `potplayer` |
| `bucket`  | `extras`    |


### Notepad3

简洁，美观的文本编辑软件。

```powershell
scoop install extras/notepad3
```

| `install` | `scoop`    |
| --------- | ---------- |
| `scoop`   | `notepad3` |
| `bucket`  | `extras`   |


## 网络

### Clash Verge

Windows 端最好用的代理工具，稳如老狗。

```powershell
scoop install extras/clash-verge
```

| `install` | `scoop`       |
| --------- | ------------- |
| `scoop`   | `clash-verge` |
| `bucket`  | `extras`      |

## 娱乐

### Mozilla Firefox

黑客用的 Web 浏览器！

```powershell
scoop install extras/firefox
```

| `install` | `scoop`   |
| --------- | --------- |
| `scoop`   | `firefox` |
| `bucket`  | `extras`  |


### Google Chrome

最有脸面的 Web 浏览器。

```powershell
scoop install extras/googlechrome
```

| `install` | `scoop`        |
| --------- | -------------- |
| `scoop`   | `googlechrome` |
| `bucket`  | `extras`       |


### QQ

功能丰富的通讯软件。

```powershell
scoop bucket add abgox_abyss https://github.com/abgox/abyss
scoop install abgox_abyss/Tencent.QQ.NT
```

| `install`     | `scoop`                          |
| ------------- | -------------------------------- |
| `scoop`       | `Tencent.QQ.NT`                  |
| `bucket`      | `abgox_abyss`                    |
| `bucket_link` | <https://github.com/abgox/abyss> |


### 微信

简单的通讯软件。

```powershell
scoop bucket add abgox_abyss https://github.com/abgox/abyss
scoop install abgox_abyss/Tencent.WeChat.Universal
```

| `install`     | `scoop`                          |
| ------------- | -------------------------------- |
| `scoop`       | `Tencent.WeChat.Universal`       |
| `bucket`      | `abgox_abyss`                    |
| `bucket_link` | <https://github.com/abgox/abyss> |


### 酷狗音乐

超前的音乐软件。

```powershell
scoop bucket add xrgzs_sdoog https://github.com/xrgzs/sdoog
scoop install xrgzs_sdoog/kugou
```

| `install`     | `scoop`                          |
| ------------- | -------------------------------- |
| `scoop`       | `kugou`                          |
| `bucket`      | `xrgzs_sdoog`                    |
| `bucket_link` | <https://github.com/xrgzs/sdoog> |


### Steam

电子游戏平台。

```powershell
scoop bucket add games
scoop install games/steam
```

| `install` | `scoop` |
| --------- | ------- |
| `scoop`   | `steam` |
| `bucket`  | `games` |

### WeGame

```powershell
scoop bucket add gendloop_gendloopBucket https://github.com/gendloop/gendloopBucket
scoop install gendloop_gendloopBucket/WeGame
```

| `install`     | `scoop`                                      |
| ------------- | -------------------------------------------- |
| `scoop`       | `WeGame`                                     |
| `bucket`      | `gendloop_gendloopBucket`                    |
| `bucket_link` | <https://github.com/gendloop/gendloopBucket> |


## 办公

### XMind

最好的思维导图软件。

```powershell
scoop bucket add extras
scoop install extras/xmind
```

| `install` | `scoop`  |
| --------- | -------- |
| `scoop`   | `xmind`  |
| `bucket`  | `extras` |


### Typora

最稳定的 Markdown 编辑软件。

```powershell
scoop install extras/typora
```

| `install` | `scoop`  |
| --------- | -------- |
| `scoop`   | `typora` |
| `bucket`  | `extras` |


### LibreOffice

```powershell
scoop install extras/libreoffice
```

| `install` | `scoop`       |
| --------- | ------------- |
| `scoop`   | `libreoffice` |
| `bucket`  | `extras`      |


## 开发工具

### VirtualBox

```powershell
scoop bucket add nonportable
scoop install nonportable/virtualbox-np
```

| `install` | `scoop`         |
| --------- | --------------- |
| `scoop`   | `virtualbox-np` |
| `bucket`  | `nonportable`   |


### Powershell

```powershell
scoop install main/pwsh
```

| `install` | `scoop` |
| --------- | ------- |
| `scoop`   | `pwsh`  |
| `bucket`  | `main`  |


### VSCode

```powershell
scoop install extras/vscode
```

| `install` | `scoop`  |
| --------- | -------- |
| `scoop`   | `vscode` |
| `bucket`  | `extras` |


### GCC

```powershell
scoop install main/gcc
```

| `install` | `scoop` |
| --------- | ------- |
| `scoop`   | `gcc`   |
| `bucket`  | `main`  |


### Qt

开源，跨平台，功能丰富强大的 C++ 软件开发框架。

- 下载链接：<https://download.qt.io/official_releases/online_installers/qt-online-installer-windows-x64-online.exe>

```powershell
$setupFileName="qt-setup"; curl "https://download.qt.io/official_releases/online_installers/qt-online-installer-windows-x64-online.exe" -C - -L -o "$env:TEMP/$setupFileName.exe"; Start-Process -FilePath "$env:TEMP/$setupFileName.exe" -Verb RunAs
```

| `download`    | `direct_link`                                                |
| ------------- | ------------------------------------------------------------ |
| `direct_link` | <https://download.qt.io/official_releases/online_installers/qt-online-installer-windows-x64-online.exe> |


### pnpm

[pnpm](https://pnpm.io/)：一款快速且节省磁盘空间的 Node 包管理器。

```powershell
scoop install main/pnpm
```

| `install` | `scoop` |
| --------- | ------- |
| `scoop`   | `pnpm`  |
| `bucket`  | `main`  |


### Node.js

作为一个异步事件驱动的 JavaScript 运行库，[Node.js](https://nodejs.org/) 旨在构建可扩展的网络应用程序。

```powershell
scoop install main/nodejs-lts
```

| `install` | `scoop`      |
| --------- | ------------ |
| `scoop`   | `nodejs-lts` |
| `bucket`  | `main`       |


### Git

[Git](https://git-scm.com/) 是一个[免费且开源](https://git-scm.cn/about/#free-and-open-source)的分布式版本控制系统，旨在快速高效地处理从小型到非常大型的项目。

```powershell
scoop install main/git
```

| `install` | `scoop` |
| --------- | ------- |
| `scoop`   | `git`   |
| `bucket`  | `main`  |


### CMake

[CMake](https://cmake.org/)：一套用于构建、测试和打包软件的工具家族。

```
scoop install main/cmake
```

| `install` | `scoop` |
| --------- | ------- |
| `scoop`   | `cmake` |
| `bucket`  | `main`  |


### Make

```powershell
scoop install main/make
```

| `install` | `scoop` |
| --------- | ------- |
| `scoop`   | `make`  |
| `bucket`  | `main`  |


### Python

一种编程语言，助您高效工作并更有效地集成系统。

```powershell
scoop install main/python
```

| `install` | `scoop`  |
| --------- | -------- |
| `scoop`   | `python` |
| `bucket`  | `main`   |


### touch

```powershell
scoop install main/touch
```

| `install` | `scoop` |
| --------- | ------- |
| `scoop`   | `touch` |
| `bucket`  | `main`  |


### CLion

```powershell
scoop install extras/clion
```

| `install` | `scoop`  |
| --------- | -------- |
| `scoop`   | `clion`  |
| `bucket`  | `extras` |


### aria2

```powershell
scoop install main/aria2
```

| `install` | `scoop` |
| --------- | ------- |
| `scoop`   | `aria2` |
| `bucket`  | `main`  |


### WSL

```powershell
winget install Microsoft.WSL
```

| `install` | `winget`        |
| --------- | --------------- |
| `winget`  | `Microsoft.WSL` |


### GDB

```powershell
scoop install main/gdb
```

| `install` | `scoop` |
| --------- | ------- |
| `scoop`   | `gdb`   |
| `bucket`  | `main`  |


## 其他

### FreeFileSync

文件同步工具。

```powershell
$html = curl -s https://freefilesync.org/download.php; $downloadLink = $html | Select-String -Pattern 'href="(\/download\/FreeFileSync_[\d\.]+_Windows_Setup\.exe)"' | ForEach-Object { $_.Matches.Groups[1].Value }; $downloadLink = "https://freefilesync.org" + $downloadLink; Write-Host "Downlod Link: $downloadLink";$setupFileName="freefilesync-setup"; curl $downloadLink -C - -L -o "$env:TEMP/$setupFileName.exe"; Start-Process -FilePath "$env:TEMP/$setupFileName.exe" -Verb RunAs
```

| `download`      | `dynamic_link`                                               |
| --------------- | ------------------------------------------------------------ |
| `dynamic_link`  | <https://freefilesync.org/download.php>                      |
| `regex`         | `href="(\/download\/FreeFileSync_[\d\.]+_Windows_Setup\.exe)"` |
| `download_link` | `"https://freefilesync-setup" + regex`                       |


### Caesium Image Compressor

批量图片压缩。

```powershell
scoop install extras/caesium-image-compressor
```

| `install` | `scoop`                    |
| --------- | -------------------------- |
| `scoop`   | `caesium-image-compressor` |
| `bucket`  | `extras`                   |


### FFmpeg

音视频文件处理工具。

```powershell
scoop install main/ffmpeg
```

| `install` | `scoop`  |
| --------- | -------- |
| `scoop`   | `ffmpeg` |
| `bucket`  | `main`   |


### ImageMagick

图片文件处理工具。

```powershell
scoop install main/imagemagick
```

| `install` | `scoop`       |
| --------- | ------------- |
| `scoop`   | `imagemagick` |
| `bucket`  | `main`        |


### LocalSend

局域网传输文件。

```powershell
scoop install extras/localsend
```

| `install` | `scoop`     |
| --------- | ----------- |
| `scoop`   | `localsend` |
| `bucket`  | `extras`    |


### OBS Studio

专业，开源的录屏工具。

```powershell
scoop install extras/obs-studio
```

| `install` | `scoop`      |
| --------- | ------------ |
| `scoop`   | `obs-studio` |
| `bucket`  | `extras`     |


### scrcpy

开源，轻量的手机投屏工具。

```powershell
scoop install main/scrcpy
```

| `install` | `scoop`  |
| --------- | -------- |
| `scoop`   | `scrcpy` |
| `bucket`  | `main`   |


### Upscayl

图片无损放大工具。

```powershell
scoop install extras/upscayl
```

| `install` | `scoop`   |
| --------- | --------- |
| `scoop`   | `upscayl` |
| `bucket`  | `extras`  |


### Keyviz

键盘可视化工具。

```powershell
scoop install extras/keyviz
```

| `install` | `scoop`  |
| --------- | -------- |
| `scoop`   | `keyviz` |
| `bucket`  | `extras` |


### MacType

Windows 字体渲染效果增强工具。

```powershell
scoop install nonportable/mactype-np
```

| `install` | `scoop`       |
| --------- | ------------- |
| `scoop`   | `mactype-np`  |
| `bucket`  | `nonportable` |


### fastfetch

轻量级的系统信息检测工具，能够快速显示系统硬件配置、操作系统信息等。

```powershell
scoop install main/fastfetch
```

| `install` | `scoop`     |
| --------- | ----------- |
| `scoop`   | `fastfetch` |
| `bucket`  | `main`      |


### pandoc

```powershell
scoop install main/pandoc
```

| `install` | `scoop`  |
| --------- | -------- |
| `scoop`   | `pandoc` |
| `bucket`  | `main`   |


### Everything

搜索本地文件，极快的搜索速度。

```powershell
scoop install extras/everything
```

| `install` | `scoop`      |
| --------- | ------------ |
| `scoop`   | `everything` |
| `bucket`  | `extras`     |


### Geek Uninstaller

```powershell
scoop install extras/geekuninstaller
```

| `install` | `scoop`           |
| --------- | ----------------- |
| `scoop`   | `geekuninstaller` |
| `bucket`  | `extras`          |


### Quicklook

```powershell
scoop install extras/quicklook
```

| `install` | `scoop`     |
| --------- | ----------- |
| `scoop`   | `quicklook` |
| `bucket`  | `extras`    |


### SumatraPDF

轻量的 PDF 阅读软件。

```powershell
scoop install extras/sumatrapdf
```

| `install` | `scoop`      |
| --------- | ------------ |
| `scoop`   | `sumatrapdf` |
| `bucket`  | `extras`     |


### Readest

现代化的电子书阅读器，支持多种电子书格式，提供舒适的阅读体验。

```powershell
scoop install extras/readest
```

| `install` | `scoop`   |
| --------- | --------- |
| `scoop`   | `readest` |
| `bucket`  | `extras`  |


### Motrix

```powershell
scoop install extras/motrix
```

| `install` | `scoop`  |
| --------- | -------- |
| `scoop`   | `motrix` |
| `bucket`  | `extras` |


### qBittorrent Enhanced Edition

开源的 BT 下载器 qBittorrent 的增强版。

```powershell
scoop install extras/qbittorrent-enhanced
```

| `install` | `scoop`                |
| --------- | ---------------------- |
| `scoop`   | `qbittorrent-enhanced` |
| `bucket`  | `extras`               |


### PixPin

截图软件，功能齐全。

```powershell
scoop bucket add abgox_abyss https://github.com/abgox/abyss
scoop install abgox_abyss/PixPin.PixPin
```

| `install`     | `scoop`                          |
| ------------- | -------------------------------- |
| `scoop`       | `PixPin.PixPin`                  |
| `bucket`      | `abgox_abyss`                    |
| `bucket_link` | <https://github.com/abgox/abyss> |


## 字体

### Maple-Mono-NF-CN

```powershell
scoop bucket add nerd-fonts
scoop install nerd-fonts/Maple-Mono-NF-CN
```

| `install` | `scoop`            |
| --------- | ------------------ |
| `scoop`   | `Maple-Mono-NF-CN` |
| `bucket`  | `nerd-fonts`       |


### Resource Han Rounded CN

```powershell
$html = curl -s -L "https://github.com/CyanoHao/Resource-Han-Rounded/releases/latest"; $version = $html | Select-String -Pattern '<h1 data-view-component="true" class="d-inline mr-3">Resource Han Rounded ([\d\.]+)</h1>' |  ForEach-Object { $_.Matches.Groups[1].Value }; Write-Host "Latest version: $version"; $downloadLink = "https://github.com/CyanoHao/Resource-Han-Rounded/releases/download/v$version/RHR-CN-$version.7z"; Write-Host "Download Link: $downloadLink"; $fontZipName = "resource-han-rounded-cn"; curl $downloadLink -C - -L -o "$env:TEMP/$fontZipName.7z"; 7z x "$env:TEMP/$fontZipName.7z" -o"$env:TEMP/$fontZipName"; $destDir = "C:\Windows\Fonts"; Get-ChildItem -Path "$env:TEMP/$fontZipName" -Recurse -Filter "*.ttf" | ForEach-Object { $destPath = Join-Path -Path $destDir -ChildPath $_.Name; Copy-Item -Path $_.FullName -Destination $destPath -Force; Write-Host "copy: $($_.Name)" }
```

| `download`       | `dynamic_link`                                               |
| ---------------- | ------------------------------------------------------------ |
| `dynamic_link`   | <https://github.com/CyanoHao/Resource-Han-Rounded/releases/latest> |
| `regex`          | `href="\/CyanoHao\/Resource-Han-Rounded\/releases\/tag\/v([\d\.]+)"` |
| `download_link`  | `"https://github.com/CyanoHao/Resource-Han-Rounded/releases/download/v" + regex + "/RHR-CN-" + regex + ".7z"` |
| `after_download` | `font_install`                                               |
