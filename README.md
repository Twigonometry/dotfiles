# dotfiles

Cybersecurity based dotfiles in `.kali-zshrc` which works with the base Kali install.

Dotfiles for Ubuntu in `.ubuntu-bashrc`.

Make sure you clone this repository inside your `~/Documents` folder so that `updaterc` alias works.

```bash
$ cd ~/Documents
$ git clone git@github.com:Twigonometry/dotfiles.git
```

If on Kali, simply sourcing `.kali-zshrc` will work, as OMZ is already installed:

```bash
$ cp ~/Documents/dotfiles/.kali-zshrc ~/.zshrc
$ source ~/.zshrc
```

If installing for Ubuntu, requires installing oh-my-zsh, so run `install.sh`:

```bash
$ chmod +x install.sh
$ ./install.sh
```

This will automatically install Docker and source the file for you (no need to run `go.zsh` manually, as this is run by the install script as I'm not good enough at Linux to figure out how to run sh commands and switch to a zsh shell to source the file from within the same script...)

If the shell is still bash, you need to [login again](https://askubuntu.com/questions/195361/chsh-s-usr-bin-zsh-not-working)!

Once sourced, any updates you can get by pulling the repo and running `updaterc`.

## Key Additions

### nfast()

Quickly scans a host with nmap - does all ports with a high minimum rate, good for CTFs

### g()

Shortcut for git, from https://github.com/thoughtbot/dotfiles

### listen()

Creates a netcat listener. Listens on 9001 with no args, or on a port of your choice with an arg

### websrv

Alias that launches a python server on `80` in `~/Documents/web/`. Put common enumeration/pivoting files here such as chisel, linpeas, etc. Other aliases assume that certain files are in here with a specific name. Python may need capabilities to run on port 80 without `sudo` but this is included by default on Kali

### pysrv

Python server in current directory

### chiselsrv

Starts a chisel server in reverse mode

### run-ghidra

Runs ghidra...

### \*.vpn

These aliases launch openvpn with a variety of `.ovpn` files. Rename your HTB season, TryHackMe, etc ovpn files as described for these aliases to work

### updaterc

Sources the `.zshrc` file because I'm not enough of a Linux power user to be bothered with an install script just yet

### mcd

Standard `mkdir` and `cd` alias

## Roadmap

- [ ] Improve prompt 💀
  - [x] Strip the guff from the Kali prompt (multi lines, skull emojis etc)
  - [x] Add the IP of tun0 if it's connected
  - [ ] Shorten the filepath if it's going to make the prompt very long (as we're now working on one line)
- [ ] Install script
  - [ ] Give python necessary capabilities
  - [ ] Output suggested commands to download good scripts for `~/Documents/web/` e.g. `wget https://github.com/jpillora/chisel/releases/download/v1.8.1/chisel_1.8.1_linux_arm64.gz -O ~/Documents/web/chisel_linux_64.gz && gunzip ~/Documents/web/chisel_linux_64.gz`
