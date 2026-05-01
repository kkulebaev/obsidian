Зайти в конфиг
```sh
nano ~/.zshrc
```
## Common
alias cp='cp -r'
alias scp='scp -r'
alias rm='rm -r'
alias mkdir='mkdir -p'
alias ls='ls -F --color=auto'
alias la='ls -A --color=auto'
alias ll='ls -l --color=auto -h'
alias lla='ll -A --color=auto -h'
alias grep='grep --color=auto'
alias open='xdg-open .'

## Neofetch
alias n="neofetch"
alias k="uname -rs"
alias g="gnome-shell --version"
alias f="lsb_release -sd"

## VPN
alias vpnon="sudo wg-quick up /etc/wireguard/wgclient_11.conf"
alias vpnoff="sudo wg-quick down /etc/wireguard/wgclient_11.conf"
