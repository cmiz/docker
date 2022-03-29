# Docker - ローカル開発環境

## 起動
```
> cd docker
> docker-compose up -d
```

## コンテナログイン
```shell
> docker-compose exec web bash
```

## hosts
```
127.0.0.1  local.test.site
```

## Apache
- https://local.test.site

## Mailhog
- http://localhost:8025

## MySQL
jdbc:mysql://localhost:3306/docker

## 停止
```
> docker-compose down
```
