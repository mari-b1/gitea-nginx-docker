# Docker-Compose-Gitea-nginx

Инструкция по запуску docker-compose.yaml в котором будет подниматься сервис gitea со следующими требованиями к сервису:
- данные содержащиеся в репозитории должны храниться на хостовом сервере
- перед сервисом gitea должен быть запущен реверс прокси
- доступ к сервису должен осуществляться по протоколу https

A Docker Compose file for Gitea - Git with a cup of tea

## Требования

Предустановленные:
* docker
* docker-compose

## Getting Started

1. Скачать файлы docker-compose.yaml и nginx.conf в рабочую директорию
2. Запустить контейнеры
```
$ docker-compose up -d
```
Проверить, что все работает
```
$ docker ps
```
3. Открыть в браузере установщик сервиса Gitea [http://localhost:3000](http://localhost:3000) и установить сервис.
