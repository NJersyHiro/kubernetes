# **3.8.1**: Docker Bench for Security

* `etc_docker_daemon.json`: ベンチマークに利用した `/etc/docker/daemon.json` (リスト243) です。
ベンチマークに利用したdockerコマンドのフラグは次のとおりです

```console
$ echo $DOCKER_CONTENT_TRUST
1

$ docker network create my-network

$ docker run \
  -d \
  --name my-nginx \
  --network my-network \
  -p 192.168.42.100:10080:80 \
  --cap-drop CAP_NET_RAW \
  --read-only \
  --tmpfs /var/cache/nginx:size=512m \
  --tmpfs /tmp:size=512m \
  --tmpfs /run:size=512m \
  --cpu-shares 512 \
  --memory 1G \
  --pids-limit 100 \
  --ulimit nofile=1024:1024 \
  nginx:1.17.3-alpine
```
