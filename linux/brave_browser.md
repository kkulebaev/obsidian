Установить браузер Brave
```sh
sudo dnf install dnf-plugins-core
```

```sh
sudo dnf config-manager --add-repo https://brave-browser-rpm-release.s3.brave.com/x86_64/
```

```sh
sudo rpm --import https://brave-browser-rpm-release.s3.brave.com/brave-core.asc
```

```sh
sudo dnf install brave-browser
```

Выполнить синхронизацию настроек браузера Brave
![[assets/sync_brave_settings.png]]
После введения кода синхронизации необходимо выбрать параметр "Синхронизировать все"
![](../assets/Pasted%20image%2020240815230724.png)
Выставить Brave браузером по умолчанию
![](../assets/Pasted%20image%2020240815230913.png)