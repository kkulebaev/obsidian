Команды актуальны для версии ESLint 9

Запуск проверки
```sh
"lint": "eslint ./src"
```

Запуск проверки с исправлениями возможных проблем
```sh
"lint:fix": "eslint ./src --fix"
```

Замер времени выполнения каждого правила
```sh
"lint:performance-time": "TIMING=1 eslint ./src"
```

Печать всех правил конфига в файл
```sh
"lint:config": "eslint --print-config eslint.config.js > eslintconfig.json"
```

Визуальный инспектор для отображения текущей конфигурации
```sh
"lint:config-inspect": "eslint --inspect-config"
```