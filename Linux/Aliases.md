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

## Work
alias ifx='cd ~/develop/ifx-ui/ && yarn dev'
alias rsb='cd ~/develop/RusBonds/Frontend && yarn dev'
alias adminka='cd ~/develop/AdminTools/Frontend && yarn dev'
alias landing='cd ~/develop/RuData_Web/RuData.Landing && yarn dev'
alias pub='cd ~/develop/publishing-ui/ && USE_DEV_PROXY=true npm run dev'

## Neofetch
alias n="neofetch"
alias k="uname -rs"
alias g="gnome-shell --version"
alias f="lsb_release -sd"

## VPN
alias vpnon="sudo wg-quick up /etc/wireguard/wgclient_11.conf"
alias vpnoff="sudo wg-quick down /etc/wireguard/wgclient_11.conf"
