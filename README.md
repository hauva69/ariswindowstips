# Ari's Windows Tips

I have for maintained a collection of [UNIX
Tips](https://github.com/hauva69/arisunixtips) for some years and UNIX type
operating system have been my choice for three decades. However, after I started
playing correspondence chess on [International Correspondence Chess
Federation](https://www.iccf.com/) the open source chess database [Scid vs.
PC](http://scidvspc.sourceforge.net/) was no longer quite enough. So instead of
installing [Xubuntu](https://xubuntu.org/) on my new laptop I left Windows 10 on
it, in order to be able to use the premier chess database
[Chessbase](https://en.chessbase.com/). Instead of building a dual boot system I
decided to give Windows 10 and [Windows Subsystem for Linux
2](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
a chance.

Do bear in mind that this is a personal document and the last time I have really administrated Windows systems was 
when Windows NT4 was brand new. That makes me a complete beginner as far as modern Windows systems are concerned.

## Docker

### Deleting all images and containers

[docker-clear.bat](https://gist.github.com/daredude/045910c5a715c02a3d06362830d045b6)

```powershell
@echo off
FOR /f "tokens=*" %%i IN ('docker ps -aq') DO docker rm %%i
FOR /f "tokens=*" %%i IN ('docker images --format "{{.ID}}"') DO docker rmi %%i
```

## Git Bash

While [Git](https://git-scm.com/) is an excellent version control system, it also provides a reasonable collection
of UNIX command line tools including vim, cut, ssh, openssl, awk and grep. If you're an UNIX dinosaur like me, do install it.

## Setting the Path

I needed Python interpreter, but after the installation the Python executable was not in my path. It turned aout, that 
there are several ways of setting the path.

- [Set path from command line](https://www.windows-commandline.com/set-path-command-line/)
- [Manage the Windows PATH environment variable with PowerShell](https://searchitoperations.techtarget.com/answer/Manage-the-Windows-PATH-environment-variable-with-PowerShell)

## Python

Add Python directories to your path, for example:

- c:\users\ari\AppData\Local\Programs\Python\Python38-32
- c:\users\ari\AppData\Local\Programs\Python\Python38-32\Scripts

## Using an Android Tablet as Second Monitor

My laptop has a 14" screen and for what I do need a dual, preferably three,
monitor system so I started to wonder whether I could use my Android tablet as a
second monitor. After very little googling I found the page [6 Ways to Use Your
Android as Second Monitor For Your
Computer](https://techwiser.com/use-your-android-as-second-monitor/). I ended up
installing [Splashtop Wired XDisplay
Free](https://play.google.com/store/apps/details?id=com.splashtop.xdisplay.wired.free)
which seemed to work well enough with my low end tablet, so I paid 7.99 € for
the version in which the session is not limited to ten minutes.

## Windows Subsystem for Linux (WSL)

WSL 2, release in May of 2020, provides a way of running a full Linux
enviroments on top of Windows provided that the build of Windows 10 is
[recent enough (Version 2004, Build 19041 or
higher)](https://docs.microsoft.com/en-us/windows/wsl/wsl2-index).

### Listing the installed Linux systems

```powershell
PS C:\Users\hauva> wsl --list
Windows Subsystem for Linux Distributions:
Ubuntu-20.04 (Default)
PS C:\Users\hauva> wsl --list --verbose
  NAME            STATE           VERSION
* Ubuntu-20.04    Running         2
```

### Setting the WSL version of a Linux system

```powershell
wsl --set-version Ubuntu-20.04 2
```

### Shutting down Linux systems

```powershell
wsl --shutdown
```

### Shutting down everything

```powershell
wsl -t <DistroName>
```

### Running screen under WSL

`screen` fails to start under Ubuntu 20.04 complaining about the rights of directory */run*.

```bash
sudo /etc/init.d/screen-cleanup start
screen
```

And, voilà, screen works.
