# **4.1.1**: シークレットファイルを扱う (`docker build --secret`)

* `etc_docker_daemon.json`: DockerデーモンのBuildKitモードを有効化するための `/etc/docker/daemon.json` の設定例 (リスト255) です。

* `git/Dockerfile`: Dockerfile中で、プライベートなGitリポジトリ `git.example.com/foo/bar.git` にアクセスする例 (リスト256) です。
  Gitリポジトリのパスは適当に置き換えてください。

使用方法:
```console
$ docker build -t foo --secret id=ssh,src=$HOME/.ssh/id_rsa .
```

* `s3/Dockerfile`: Dockerfile中で、プライベートなS3バケット `examplebucket` にアクセスする例 (リスト258) です。
  バケット名は適当に置き換えてください。

使用方法:
```console
$ docker build -t foo --secret id=aws,src=$HOME/.aws/credentials .
```
