# Docker-Compose-Gitea

docker-compose.yaml в котором будет пониматься сервис gitea со следующими требование к сервису:
- данные содержащиеся в репозитории должны храниться на хостовом сервере
- перед сервисом gitea должен быть запущен реверс прокси
- доступ к сервису должен осуществляться по протоколу https

A Docker Compose file for Gitea - Git with a cup of tea

Data will be saved in separate docker volumes to enable easy upgrades!

## Requirements

* docker
* docker-compose

## Getting Started

1. Create a file named docker-compose.yaml and copy the above code into it.
2. Replace /path/to/repositories with the path to the directory where you want to store your repositories on the host machine.
3. Run docker-compose up -d to start the services in detached mode.
4. Access Gitea at https://localhost.

1. Copy **.env.dist** to **.env** and make your modifications
2. Start docker containers:
```
$ docker-compose up -d
```

After that open gitea installer via browser: [http://localhost:3000](http://localhost:3000) and fill the form according your .env settings. 

Set **`gitea-db:3306`** in _Host_ field and complete setup.

After setup is completed register a new user (use link from the navigation bar).

The first registered user has admin privileges.


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


