Запустить контейнер с образом `posgres` и названием `guardian-of-finance-db`, где будет переменная окружения `POSTGRES_PASSWORD=qwerty123`
```sh
docker run --name=db-container -e POSTGRES_PASSWORD='qwerty123' -p 5436:5432 -d --rm postgres
```

Подключаемся к контейнеру
```sh
docker exec -it [CONTAINER_ID] /bin/bash
```

Подключаемся к postgres
```sh
psql -U postgres
```

Посмотреть список БД
```sh
\l
```

Посмотреть список таблиц
```sh
\d
```

Создать БД
```sh
create database [DB_NAME];
```

Подключиться к БД
```sh
\c [DB_NAME]
```

Создать таблицу
```sh
create table [TABLE_NAME] (id serial not null unique, first_name varchar(255) not null, last_name varchar(255) not null);
```

Вставить в таблицу строку
```sh
insert into [TABLE_NAME] (first_name, last_name) values ('Konstantin', 'Kulebaev');
```

Получить данные из таблицы
```sh
select * from [TABLE_NAME];
```

Обновить данные в строке
```sh
update [TABLE_NAME] set [COLUMN_NAME]=[NEW_VALUE] where id=1
```
