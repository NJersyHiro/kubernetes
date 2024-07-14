# **3.4.4**: ファイルアクセスを細かく制御する (SELinux)

* `foo.cil`: 「プロセスのドメインを定義する」の項目で紹介した、`user_home_t` タイプのファイルにアクセスするためのSELinuxポリシーモジュールです。udica 0.2.0で作成 (リスト154) しました。異なるバージョンのudicaがインストールされている場合、udicaを再実行してポリシーを作り直す必要があることがあります。

使用方法:
```console
$ sudo semodule -i foo.cil /usr/share/udica/templates/base_container.cil
$ podman run --rm -v /home/exampleuser/foo:/foo \
  --security-opt label=type:foo.process docker.io/library/centos:8 ls -Z /foo
unconfined_u:object_r:user_home_t:s0 hello
```
