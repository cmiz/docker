# Docker - ローカル開発環境

## 起動
```
> cd docker
> docker-compose up -d
```

## コンテナログイン
```shell
> docker-compose exec php bash
```

## hosts
```
127.0.0.1  local.test.site
```

## Nginx
- https://local.test.site

## Maildev
- http://localhost:1080

## MySQL
jdbc:mysql://localhost:3306/docker

## 停止
```
> docker-compose down
```
