Добавить юзера в CLI
```sh
npm adduser
```

Запушить пакет (при публикации впервые нужен флаг `--access=public`)
```sh
npm publish
```

Проставить тег для обновления пакета
```sh
npm version patch // 1.0.1 
npm version minor // 1.1.0 
npm version major // 2.0.0
npm version <newversion> // произвольная версия
```

Удалить пакет из npm
```sh
npm unpublish <package-name> -f
```

Устранение дублей
```sh
npm dedupe
```
