Добавить юзера в CLI
```sh
npm adduser
```

Опубликовать пакет
```sh
npm publish --access=public
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