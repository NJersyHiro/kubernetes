# **3.4.3**: ファイルアクセスを細かく制御する (AppArmor)

* `docker-default`: DockerのデフォルトのAppArmorプロファイル (リスト136) です。
  カスタムプロファイルを作成するためのテンプレートとして使用できます。
  出典: https://github.com/docker/engine/blob/v19.03.3/profiles/apparmor/template.go (Apache License 2.0)

* `completely-read-only`: 再帰的マウントしたディレクトリ中のファイルも含め、全てのファイル書き込みを禁止するプロファイルの例 (リスト137) です。

  使用方法:
```console
$ sudo apparmor_parser completely-read-only
$ docker run --rm -v /:/host --security-opt apparmor=completely-read-only alpine touch /host/mnt/usb/foo
touch: /host/mnt/usb/foo: Permission denied
```

* `apparmor-runtime-default`: KubernetesのPodマニフェスト中で、CRIランタイムのデフォルトのAppArmorプロファイルを指定する例 (リスト141を簡略化) です。
  AppArmorが有効になっていれば、プロファイル名 ("unconfined"以外の文字列) がPodのログに表示されます。無効であれば "AppArmor is not enabled on the host" のエラーでPodがblockされます。kubeletやCRIランタイムのバージョンによっては、 "unconfined" と表示されることも考えられます。
  [なお、将来のバージョンのKubernetesでは設定方法が変わる見込みです。](https://github.com/kubernetes/enhancements/pull/1444)
