# ローカル開発環境（自力docker）

---
### コンテナ(再)ビルド
#### Mac
```shell
  docker compose build --no-cache
```
#### WSL
```shell
  HOST_UID=$(id -u) HOST_GID=$(id -g) docker compose build --no-cache
```
---
### コンテナ起動
#### Mac
```shell
  docker compose up -d
```
#### WSL
```shell
  HOST_UID=$(id -u) HOST_GID=$(id -g) docker compose up -d
```
---
### アプリケーションコンテナ入室
```shell
  docker compose exec php bash
```
---
### vendor生成
```shell
  composer install
```
---
### コンテナ退出
```
  exit (Ctrl + D)
```
---
### ブラウザ確認
- https://localhost/
---
### Mailpit
- http://localhost:8025/
---
### コンテナ停止
```shell
  docker compose down
```
---
