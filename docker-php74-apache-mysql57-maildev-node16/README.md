# Docker - ローカル開発環境

```shell
> cd docker
> docker-compose up -d
```

## hosts
```
127.0.0.1  local.test.site
```

## コンテナ
```shell
> docker-compose exec php-apache bash
```

## Apache
- https://local.test.site

## Maildev
- http://localhost:1080

## MySQL
jdbc:mysql://localhost:3306/docker

## 停止
```shell
> docker-compose down
```
