Установить openconnect (на Fedora 40 он уже есть)
```sh
sudo dnf install openconnect
```

Выбрать сервер подключения
```sh
sudo openconnect ra.interfax.ru
```

Быстрая комманда со всеми флагами
```sh
sudo openconnect ra.interfax.ru --authgroup=Multifactor --user=ku.kulebaev
```
