---
tags:
  - os
  - linux
---
# Linux Features

Most of these I already know or they are integration with Windows-based technology.

## Package Managers

The standard for Linux isn't to go to some random website and install a sketchy program, but rather install a "package" (which is a program or a collection of programs or libraries) to your system from official or (alternatively) unofficial repositories.

|Distribution|Package Manager Name|
|-|-|
|Debian Based|`apt` or `yum`|
|Arch Based|`pacman`|
|Gentoo|`emerge`|
|CentOS|`zypper` or `zipper`|
|Void Linux|`xbps`|
|Windows|`winget`|

>The `winget` package manager for Windows is relatively new actually, released in May 27, 2021. And it's [FOSS](https://github.com/microsoft/winget-cli) too.

## Other Features

Linux has antivirus programs, which I personally never use because I don't install stupid shit.

There are also GUI-based package managers you could call them.

There's also snaps and flatpaks which are another way to install applications, but I tend to avoid them. I just don't really wanna deal with them tbh.

## Windows Integration

Now, when I say integration I really just mean people have created utilities to interface with Microsoft specific protocols like [[SMB|SMB]] (Server Message Block). You can use "Samba" to turn your Linux server into something that Windows machines can easily interface with.
