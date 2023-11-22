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

1. Скачать файл .env.dist в .env и внести свои изменения.
2. Скачать файл docker-compose.yaml в рабочую директорию
3. Запустить контейнеры
```
$ docker-compose up -d
```
4. Открыть в браузере установщик сервиса Gitea в браузере [http://localhost:3000](http://localhost:3000) и заполнить форму согласно данным в файле .env
5. После завершения установка зарегистрируйте нового пользователя. Первый зарегистрированный пользователь будет иметь права администратора. 

### Environment Configuration

| VARIABLE              | Description                       | DEFAULT       |
| ----------------------|-----------------------------------|:-------------:|               
|GITEA_VERSION          | Docker-Image-Version              |latest         |
|GITEA_HOSTNAME         | Hostname for Gitea Application    |localhost      |
|GITEA_WEB_PORT         | GUI-Port for accessing Gitea      |3000           |
|GITEA_SSH_PORT         | Port for accessing Gitea via SSH  |2222           |
|MYSQL_ROOT_PASSWORD    | MySQL root password               |root           |
|MYSQL_DATABASE         | Database name for gitea           |gitea          |
|MYSQL_USER             | Database user for gitea           |gitea          |
|MYSQL_PASSWORD         | Password for MySQL user           |gitea          |


