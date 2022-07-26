---
Date: 2022-07-25
Author: Jimmy Briggs <jimmy.briggs@jimbrig.com>
Tags: ["#Type/Code/Bash", "#Topic/Dev/Linux"]
Alias: []
---

# Bash - Install Zsh

*Source: [Installing ZSH · ohmyzsh/ohmyzsh Wiki · GitHub](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)*

```bash

```



## Install and set up Zsh as default

If necessary, follow these steps to install Zsh:

1.  There are two main ways to install Zsh:
    
    -   With the package manager of your choice, _e.g._ `sudo apt install zsh` (see [below for more examples](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#how-to-install-zsh-on-many-platforms))
    -   From [source](https://zsh.sourceforge.io/Arc/source.html), following [the instructions from the Zsh FAQ](https://zsh.sourceforge.io/FAQ/zshfaq01.html#l7).
2.  Verify installation by running `zsh --version`. Expected result: `zsh 5.0.8` or more recent.
    
3.  Make it your default shell: `chsh -s $(which zsh)`
    
    -   Note that this will not work if Zsh is not in your authorized shells list (`/etc/shells`) or if you don't have permission to use `chsh`. If that's the case [you'll need to use a different procedure](https://www.google.com/search?q=zsh+default+without+chsh).
4.  Log out and log back in again to use your new default shell.
    
5.  Test that it worked with `echo $SHELL`. Expected result: `/bin/zsh` or similar.
    
6.  Test with `$SHELL --version`. Expected result: 'zsh 5.8' or similar
    

## [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#how-to-install-zsh-on-many-platforms)How to install zsh on many platforms

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#macos)macOS

**Try `zsh --version` before installing it from Homebrew. Preferably newer than or equal to `5.0.8`.**

brew install zsh

To set zsh as your default shell, execute the following assuming a default install of Homebrew

-   Recent macOS versions:
    
    chsh -s /usr/local/bin/zsh
    
-   macOS **High Sierra** and older:
    
    chsh -s /bin/zsh
    

Assuming you have [Homebrew](https://brew.sh/) installed. If not, most versions of **macOS** ship zsh by default, but it's normally an older version. Alternatively, you may also use [MacPorts](https://www.macports.org/)

sudo port install zsh zsh-completions

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#ubuntu-debian--derivatives-windows-10-wsl--native-linux-kernel-with-windows-10-build-1903)Ubuntu, Debian & derivatives (Windows 10 WSL | Native Linux kernel with Windows 10 build 1903)

apt install zsh

If you don't have `apt`, the recommended package manager for end users [[1]](https://askubuntu.com/a/446484) [[2]](https://askubuntu.com/a/775264) [[3]](https://help.ubuntu.com/lts/serverguide/apt.html) [[4]](https://www.howtogeek.com/234583/simplify-command-line-package-management-with-apt-instead-of-apt-get/) , you can try `apt-get` or `aptitude`.

[Other distributions that apply](https://en.wikipedia.org/wiki/List_of_Linux_distributions#Debian-based) include: Linux Mint, elementary OS, Zorin OS, Raspbian, MX Linux, Deepin.

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#opensuse)OpenSUSE

zypper install zsh

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#arch-linux-or-manjaro)Arch Linux or Manjaro

pacman -S zsh

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#void-linux)Void Linux

xbps-install zsh

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#fedora)Fedora

dnf install zsh

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#openbsd)OpenBSD

To install the package:

pkg_add zsh

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#freebsd)FreeBSD

To install the package:

pkg install zsh

To install the port:

cd /usr/ports/shells/zsh/ && make install clean

To reduce memory usage, optionally enable zsh-mem options with ![installation screen to enable zsh-mem](https://camo.githubusercontent.com/68720a867a939ffaf119cfbddb8d4aa64670b3366f22e20793fbaa36a064f0cd/68747470733a2f2f692e696d6775722e636f6d2f6c34696436456b2e706e67)

make config

before running "make install".

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#centosrhel)Centos/RHEL

sudo yum update && sudo yum -y install zsh

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#cygwin)Cygwin

Install the zsh package using the installer. Unfortunately Cygwin doesn't have a standard command line interface. You could, however, setup [apt-cyg](https://github.com/kou1okada/apt-cyg) and install zsh as follows:

apt-cyg install zsh

The easiest way to change the default shell is to set your SHELL user environment variable. Search for "Edit Environment variables for your account" to bring up the environment variables window, create a new variable named "SHELL" and give it the value "/usr/bin/zsh/".

_Alternatively:_ Open Cygwin (in BASH) then type:

sudo nano ~/.bashrc

Once the .bashrc file is open, add this line to the very top:

exec zsh

Close and save the file. Close and reopen Cygwin. It will execute the command every time you load the terminal and run your zsh shell.

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#solus)Solus

eopkg it zsh

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#funtoogentoo)Funtoo/Gentoo

emerge app-shells/zsh

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#alpine-linux)Alpine Linux

apk add zsh

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#msys2)MSYS2

pacman -S zsh

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#termux-android)Termux (Android)

Termux is an terminal emulator for Android but has modern feature like Debian and Ubuntu (Termux has Bash shell and Busybox GNU-like programs). For the package manager, Termux using an Debian/Ubuntu package manager, APT. To install the package, run this command:

pkg install zsh

The command looks like FreeBSD package manager (`pkg`). Or you can run this command:

apt update && apt upgrade
apt install zsh

To set zsh as your default shell, run this command:

chsh -s zsh

### [](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH#kiss-linux)KISS Linux

To install zsh, you must add the [community](https://github.com/kiss-community/repo-community/) repo to your `$KISS_PATH`.

kiss b zsh && kiss i zsh

***

## Appendix: Links and References

- [[Code]]
- [[Development]]
- [[Linux]]
- [[2-AREAS/Code/Bash/_README|Bash]]

***

Jimmy Briggs <jimmy.briggs@jimbrig.com> | 2022