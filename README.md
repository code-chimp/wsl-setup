# WSL Setup - Using Ubuntu 18.04

## Windows

### Environment prep

#### Fix terminal colors to make bash prompt more readable

1. Clone https://github.com/wbkang/cmd-colors-solarized
1. Double-click `almost-ubuntu.reg`

#### Install Powerline fonts for airline

1. Download and install the [Ubuntu Font Family](https://design.ubuntu.com/font/)
1. Clone https://github.com/powerline/fonts
1. Run `install.ps1` to install all of the fonts

## Linux

### Install default packages

```
$ sudo apt update && sudo apt dist-upgrade -y
$ sudo apt install golang-go python python-pip apt-transport-https software-properties-common ca-certificates curl tmux mercurial subversion tree
```

### Some tools to setup

1. [vim-plug](https://github.com/junegunn/vim-plug)
1. [Node Version Manager](https://github.com/creationix/nvm)
1. [tmux Package Manager](https://github.com/tmux-plugins/tpm)
2. [fzf: command-line fuzzy finder](https://github.com/junegunn/fzf) __my vimrc + vim-plug will set this up__
3. ... and copy the configs to `~`

### Configure Docker pass-through

[Setting Up Docker for Windows and WSL to Work Flawlessly](https://nickjanetakis.com/blog/setting-up-docker-for-windows-and-wsl-to-work-flawlessly)

## Reference(s)

* [Nick Janetakis' WSL Article](https://nickjanetakis.com/blog/a-linux-dev-environment-on-windows-with-wsl-docker-tmux-and-vscode)
