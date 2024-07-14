# **3.1.3**: コンテナ内からDocker APIを呼び出す

* `dood.yaml`: "Docker-outside-of-Kubernetes" のマニフェスト例 (リスト69) です。
  `docker info` のコマンドは適当に書き換えてください。

* `dind.yaml`: "Docker-in-Kubernetes" のマニフェスト例 (リスト73) です。
  テキストでは省略しましたが、`.spec.volumes[].secret.secretName` に `ca.pem`、`cert.pem`、`key.pem` を含む Secret を指定してください。
