# Preference
- 言語を英語（米国）に設定
- Control Panel > Sound > システム音を切る
- Google日本語入力
    - スペース等全角禁止
    - Ctrl+Spaceで切り替え http://d.hatena.ne.jp/ang65/20110409/1302316109
- Control Panel > Keyboard からキーリピートを最速に
- One DriveをUninstall


# Chololatery
https://chocolatey.org/

管理者権限アリの `cmd.exe` からInstall。

```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```


# Download
```
# Git for windows
https://gitforwindows.org/

# Sourcetree
https://ja.atlassian.com/software/sourcetree

# Google chrome
https://www.google.com/intl/ja_ALL/chrome/

# vscode
https://code.visualstudio.com/download

# FileZilla
https://filezilla-project.org/download.php?type=client

# TextExpander
https://textexpander.com/download/

# TeamViewer
https://www.teamviewer.com/ja/

# openFrameworks
https://openframeworks.cc/download/

# Visual Studio Community 2017 ( ... don't forget disable automatic precompiled header)
https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=Community&rel=15

# Spotify
https://www.spotify.com/jp/download/windows/

# K-lite codec pack Mega
https://www.codecguide.com/download_k-lite_codec_pack_mega.htm

# Dropbox
https://www.dropbox.com/install

# Microsoft Office
https://account.microsoft.com/services/office/install

# Voicemeeter
https://www.vb-audio.com/Voicemeeter/

```


# rsyncを使ったバックアップ環境つくり

- Windows Subsystem for Linux(WSL)を入れる。DistributionはとりあえずUbuntu。
- Windows開発者モードをONにする
- コマンドプロンプトからUbuntuのbackport越しにrsyncを叩く

みたいな事をやるshell scriptをWindows側に作っておけばダブルクリックでバックアップ完了。

Example: Local Fドラを家Backup serverのEドラにまるごとバックアップ

`$ wsl rsync -av --delete -e ssh /mnt/f/ [username]@[host]:/mnt/e`