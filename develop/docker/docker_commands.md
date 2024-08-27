Вывести список образов
```sh
docker image ls
```

Вывести список запущенных контейнеров
```sh
docker ps -a
```

Останавливает контейнер
```sh
docker stop [CONTAINER_ID]
```

Запускает контейнер по ID
```sh
docker run -p 3000:3000 [IMAGE_ID]
```

Присоединяется к контейнеру по ID
```sh
docker attach [CONTAINER_ID]
```

Запускает существующий контейнер
```sh
docker start [CONTAINER_ID]
```

Запускает и удаляет контейнер с именем
```sh
docker run -p 3000:3000 -d —rm —name nodeapp IMAGE_ID
```

Создает образ с именем
```sh
docker build -t calc:latest .
```

Информация по образу
```sh
docker image inspect IMAGE
```

Смотрим, что происходит в контейнере
```sh
docker logs CONTAINER
```

Удаляем образы
```sh
docker rmi IMAGE
```

Удаляем контейнеры
```sh
docker rm CONTAINER_IDS
```

Удаляем все неиспользуемые контейнеры
```sh
docker container prune
```

Посмотреть список файлов в директории /app в контейнере по имени
```bash
docker exec -i -t [CONTAINER_NAME] ls -alF /app
```

Остановить все контейнеры
```sh
docker stop $(docker ps -a -q)
```

Удалить все контейнеры
```sh
docker rm $(docker ps -a -q)
```

Удалить все образы
```sh
docker rmi -f $(docker images -aq)
```
