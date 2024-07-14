# **3.3.2**: 不要なシステムコールの呼び出しを禁止する (seccomp)

* `docker-default-seccomp.json`: Dockerのデフォルトのseccompプロファイル (リスト117) です。
  カスタムプロファイルを作成するためのテンプレートとして使用できます。
  出典: https://github.com/docker/engine/blob/v19.03.3/profiles/seccomp/default.json (Apache License 2.0)

* `hello-world-seccomp.json`: Docker 19.03.3で、`hello-world` イメージを実行するための最小限のseccompプロファイル (リスト119) です。
  ただし、Dockerおよびruncのバージョンや設定によっては、更に多くのシステムコールを許可する必要がある場合があります。

  使用方法:
```console
$ docker run --rm --security-opt seccomp=hello-world-seccomp.json hello-world
```

* `nginx-seccomp.json`: Docker 19.03.3で、`nginx:1.17.3-alpine` イメージを実行するための最小限のseccompプロファイル (リスト121) です。
  DockerSlimを使って作成しました。`hello-world-seccomp.json` と同様、更に多くのシステムコールを許可する必要がある場合があります。

  使用方法:
```console
$ docker run --rm --security-opt seccomp=nginx-seccomp.json -p 80:80 nginx:1.17.3-alpine
```

* `seccomp-runtime-default.yaml`: KubernetesのPodマニフェスト中で、CRIランタイムのデフォルトのseccompプロファイルを指定する例 (リスト123) です。
  seccompが有効になっていれば、"Seccomp: 2" とPodのログに表示されます。無効であれば "Seccomp: 0" と表示されます。
  [なお、将来のバージョンのKubernetesでは設定方法が変わる見込みです。](https://github.com/kubernetes/enhancements/pull/1148)
