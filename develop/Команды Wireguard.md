Подключение к удаленному серверу по SHH
```sh
ssh root@[ip]
```
ssh root@95.214.8.243

Посмотреть список подключенных клиентов WireGuard
```sh
wg show
```

Создание нового подключения
```sh
cd /etc/wireguard
```

```sh
./easy-wg-quick
```

Рестарт утилиты для VPN после создания пользователя
```sh
systemctl restart wg-quick@wghub
```