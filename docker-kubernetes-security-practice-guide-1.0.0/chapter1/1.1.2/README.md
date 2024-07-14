# **1.1.2**: Dockerの使い方の復習

## `my-nginx`

「イメージを自作する」の項目で紹介した `ssl.conf` (リスト10)、`Dockerfile` (リスト11)の例です。
`ssl.conf`中のサーバ名 `my-nginx.example.com` は適当に書き換えてください。

なお、`cert.pem` 及び `key.pem` は含んでいません。テキスト**1.3.4** を参考に作成してください。

イメージビルド・起動手順:

```console
$ docker build -t my-nginx .
$ docker run -d --name my-nginx -p 0.0.0.0:443:443/tcp \
  -v $(pwd)/key.pem:/run/secrets/key.pem:ro my-nginx
```

## `docker-compose`

「コンテナ同士を通信させる」の項目で紹介した `docker-compose.yaml` (リスト23)、`ssl.conf` (リスト24)の例です。
`ssl.conf`中のサーバ名 `wordpress.example.com` は適当に書き換えてください。

なお、`cert.pem` 、 `key.pem`、`mysql-root-password`、`mysql-wp-password` は含んでいません。

起動手順:

```console
docker-compose up -d
```
