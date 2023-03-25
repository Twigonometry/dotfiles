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
