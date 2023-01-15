Устанавливаем ZSH в Fedora Linux
```sh
sudo dnf install zsh
```

Делаем ZSH по умолчанию для нашего терминала
```sh
grep tecmint /etc/passwd
```

```sh
chsh -s $(which zsh)
```

```sh
grep tecmint /etc/passwd
```

Устанавливаем фреймворк oh-my-zsh
```
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

Перезапускаем ПК
```sh
reboot
```

```
zsh
```
