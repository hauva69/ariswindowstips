# Ari's Windows Tips

I have for maintained a collection of [UNIX Tips](https://github.com/hauva69/arisunixtips) for some years 
and UNIX type operating system have been my choice for three decades. However, after I started playing 
correspondence chess on [International Correspondence Chess Federation](https://www.iccf.com/) the open 
source chess database [Scid vs. PC](http://scidvspc.sourceforge.net/) was no longer quite enough. So instead 
of installing [Xubuntu](https://xubuntu.org/) on my new laptop I left Windows 10 on it, in order to be able 
to use the premier chess database [Chessbase](https://en.chessbase.com/). Instead of building a dual boot 
system I decided to give Windows 10 and [Windows Subsystem for Linux 2](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
a chance.

Do bear in mind that this is a personal document and the last time I have really administrated Windows systems was 
when Windows NT4 was brand new. That makes me a complete beginner as far as modern Windows systems are concerned.

## Git Bash

While [Git](https://git-scm.com/) is an excellent version control system, it also provides a reasonable collection
of UNIX command line tools including vim, cut, ssh, openssl, awk and grep. If you're an UNIX dinosaur like me, do install it.

## Setting Path

I needed Python interpreter, but after the installation the Python executable was not in my path. It turned aout, that 
there are several ways of setting the path.

- [Set path from command line](https://www.windows-commandline.com/set-path-command-line/)
- [Manage the Windows PATH environment variable with PowerShell](https://searchitoperations.techtarget.com/answer/Manage-the-Windows-PATH-environment-variable-with-PowerShell)

## Python

Add Python directories to your path, for example:

- c:\users\ari\AppData\Local\Programs\Python\Python38-32
- c:\users\ari\AppData\Local\Programs\Python\Python38-32\Scripts

## Using an Android Tablet as Second Monitor

My laptop has a 14" screen and for what I do I really need a dual, preferably three, monitor system so I started to wonder whether I could use my Android tablet as a second monitor. After very little googling I found the page [6 Ways to Use Your Android as Second Monitor For Your Computer](https://techwiser.com/use-your-android-as-second-monitor/). I ended up installing [Splashtop Wired XDisplay Free](https://play.google.com/store/apps/details?id=com.splashtop.xdisplay.wired.free) which seemed to work well enough with my low end tablet, so I paid 7.99 € for the version in which the session is not limited to ten minutes.
