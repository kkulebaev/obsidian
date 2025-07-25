Вывести список связей с удаленным репозиторием
```sh
git remote -v
```

Удалить связь с удаленным репозиторием
```sh
git remote rm origin
```

Добавить связь с удаленным репозиторием
```sh
git remote add origin [URL]
```

Создать тэг
```sh
git tag [tag_name] [branch] -m "[Сообщение]"
```

Удалить тэг локально
```sh
git tag -d [tag_name]
```

Запушить тэг в репозиторий
```sh
git push origin tag [tag_name]
```

Изменить локальное имя пользователя git на проекте
```sh
git config --local user.name "Konstantin Kulebaev"
```

Изменить локальный email пользователя git на проекте
```sh
git config --local user.email "ku.kulebaev@interfax.ru" 
```

Переписать автора коммитов
```sh
git rebase -r [ID КОММИТА ДО КОТОРОГО НУЖНО МЕНЯТЬ АВТОРА (НЕ ВКЛЮЧИТЕЛЬНО)] \
    --exec 'git commit --amend --no-edit --reset-author'
```

Изменить дату последнего коммита
```sh
git commit --amend --date=now --no-edit
```

Ребейз засквошенной ветки
```
git checkout Branch-2
git rebase --onto master Branch-1
```

Запушить в удаленный репозиторий с другим именем
```
git push --force origin [ЛОКАЛЬНОЕ НАЗВАНИЕ ВЕТКИ]:[НАЗВАНИЕ ВЕТКИ В УДАЛЕННОМ РЕПО]
```
