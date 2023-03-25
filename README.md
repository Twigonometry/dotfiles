# dotfiles
Cybersecurity based dotfiles. First attempt at a dotfiles repo - likely not going to go very well

This is largely a port of the base ZSH config on Kali, so there's a lot of stuff in `.zshrc` that I don't understand and isn't necessarily useful. My stuff is at the bottom

## Key Additions

### nfast()

Quickly scans a host with nmap - does all ports with a high minimum rate, good for CTFs

### g()

Shortcut for git, from https://github.com/thoughtbot/dotfiles

### listen()

Creates a netcat listener. Listens on 9001 with no args, or on a port of your choice with an arg

### websrv

Alias that launches a python server on `80` in `~/Documents/web/`. Put common enumeration/pivoting files here such as chisel, linpeas, etc. Other aliases assume that certain files are in here with a specific name. Python may need capabilities to run on port 80 without sudo but this is included by default on Kali

### pyserv

Python server in current directory

### chiselserv

Starts a chisel server in reverse mode

### \*.vpn

These aliases launch openvpn with a variety of `.ovpn` files. Rename your HTB season, TryHackMe, etc ovpn files as described for these aliases to work

### updaterc

Sources the .zshrc file because I'm not enough of a Linux power user to be bothered with an install script just yet

### mcd

Standard `mkdir` and `cd` alias

## Roadmap

- [ ] Improve prompt
  - [ ] Strip the guff from the Kali prompt (multi lines, skull emojis etc)
  - [ ] Add the IP of tun0 if it's connected
  - [ ] Shorten the filepath if it's going to make the prompt very long (as we're now working on one line)
- [ ] Install script
  - [ ] Give python necessary capabilities
  - [ ] Output suggested commands to download good scripts for `~/Documents/web/`
