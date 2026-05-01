# Coolify

Open-source self-hosted PaaS — альтернатива Heroku, Vercel, Netlify и Railway. Работает на любом сервере с SSH (VPS, Hetzner, EC2, DigitalOcean, Raspberry Pi) и управляет деплоями через Docker. Бесплатен в self-hosted режиме без ограничений.

## Содержание

- [Архитектура](#Архитектура)
- [Иерархия объектов](#Иерархия%20объектов)
- [Build Packs](#Build%20Packs)
- [Источники кода](#Источники%20кода)
- [Поддерживаемые БД](#Поддерживаемые%20БД)
- [Сервисы one-click](#Сервисы%20one-click)
- [Ключевые фичи](#Ключевые%20фичи)
- [Установка](#Установка)
- [Когда стоит брать](#Когда%20стоит%20брать)
- [Когда не стоит](#Когда%20не%20стоит)

## Архитектура

- Ставится одной командой через bash-скрипт
- Хранит данные в `/data/coolify/` (исходники, SSH-ключи, приложения, БД, бэкапы, прокси)
- Использует Docker и Traefik (или Caddy) как реверс-прокси
- Управляет удалёнными серверами по SSH — один Coolify-инстанс может разворачивать на множество машин
- Есть облачная версия (платная), но self-hosted всегда бесплатен

## Иерархия объектов

| Уровень | Назначение |
|---|---|
| Project | верхний контейнер (например, «Pet projects» vs «Work») |
| Environment | окружение внутри проекта (`production`, `staging`) |
| Resource | конкретный объект: приложение, БД, сервис |
| Server / Destination | целевая машина и Docker-сеть для деплоя |

## Build Packs

Способы превращения исходного кода в Docker-контейнер:

1. **Nixpacks** — авто-детект стека (Node, Python, Go, Rust, PHP, Ruby...), без конфигов
2. **Static** — статические сайты и SPA
3. **Dockerfile** — полный контроль над образом
4. **Docker Compose** — мульти-сервисные стеки
5. **Pre-built Image** — деплой готового образа из реестра

## Источники кода

GitHub, GitLab, Bitbucket, Gitea — публичные и приватные репозитории. Поддерживаются:

- push-to-deploy через webhook
- PR previews — отдельный деплой на каждый pull request или коммит
- автодеплой по событиям

## Поддерживаемые БД

One-click managed-базы с автобэкапами в S3-совместимое хранилище и восстановлением:

- PostgreSQL
- MySQL / MariaDB
- MongoDB
- Redis / KeyDB / Dragonfly
- ClickHouse

## Сервисы one-click

280+ готовых шаблонов: WordPress, Ghost, n8n, Plausible, Umami, Supabase, Appwrite, Directus, MinIO, Grafana, Uptime Kuma и т.д.

## Ключевые фичи

- Автоматический Let's Encrypt SSL и продление сертификатов
- Real-time терминал в браузере
- Health checks и алерты в Discord, Telegram, Email
- Команды и роли (RBAC) — совместная работа с гранулярными правами
- REST API и webhooks для CI/CD
- Лимиты CPU/RAM на ресурс
- Без vendor lock-in: данные и контейнеры остаются на своём сервере

## Установка

Быстрая установка одной командой:

```bash
curl -fsSL https://cdn.coollabs.io/coolify/install.sh | sudo bash
```

С предзаданным админом:

```bash
env ROOT_USERNAME=admin \
  ROOT_USER_EMAIL=admin@example.com \
  ROOT_USER_PASSWORD=SecurePassword123 \
  bash -c 'curl -fsSL https://cdn.coollabs.io/coolify/install.sh | bash'
```

С отключённым автообновлением:

```bash
env AUTOUPDATE=false bash -c 'curl -fsSL https://cdn.coollabs.io/coolify/install.sh | bash'
```

## Когда стоит брать

- Хочется push-to-deploy DX как у Vercel, но на своём железе
- Нужно экономить на облаке, особенно на managed-БД
- Требуется контроль над данными (compliance, GDPR)
- Команда готова работать с Docker и SSH

## Когда не стоит

- Нужен глобальный edge/CDN из коробки
- Команда не хочет администрировать Linux-серверы
- Требуется serverless и auto-scaling «из ноля» — Coolify работает с долгоживущими контейнерами

## Ссылки

- Сайт: https://coolify.io/
- Документация: https://coolify.io/docs
- GitHub: https://github.com/coollabsio/coolify
