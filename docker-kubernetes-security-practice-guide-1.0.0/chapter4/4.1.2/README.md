# **4.1.2**: ssh-agentをフォワードする (`docker build --ssh`)

* `Dockerfile`: Dockerfile中で、ssh-agent経由でプライベートなGitリポジトリ `git.example.com/foo/bar.git` にアクセスする例 (リスト260) です。
  Gitリポジトリのパスは適当に置き換えてください。

使用方法:

```console
$ eval $(ssh-agent)
$ ssh-add ~/.ssh/id_rsa
(パスフレーズを入力する)
$ docker build -t foo --ssh default=$SSH_AUTH_SOCK .
```
