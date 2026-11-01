# Traefik

Общий прокси для локальных docker-проектов: один на машину слушает 80 и 443 и передаёт запросы контейнерам по имени домена. Проекты подключаются через сеть `bitenv-proxy` и labels в своём `docker-compose.yml`.

## Быстрый старт

```bash
docker network create bitenv-proxy   # один раз на машину
cp .env.example .env                 # необязательно: по умолчанию порты 80, 443, 8080
docker compose up -d
```

Дашборд: http://localhost:8080
