# **3.2.2**: 権限昇格を防止する (`no_new_privs` ビット)

* `no-new-privs.yaml`: KubernetesのPodマニフェスト中で `no_new_privs` ビット を有効化 (`allowPrivilegeEscalation` を `false` に指定) する例 (リスト92) です。
  例として `ping` コマンドを実行しています。
  `no_new_privs` ビットが有効であるため、`/bin/ping` バイナリに与えられた `CAP_NET_RAW` ファイルケーパビリティが無効となり、 `ping` コマンドが失敗することをログで確認してください。
  ただし、**3.3.1** で紹介する sysctlパラメータ `net.ipv4.ping_group_range` の値によっては、成功することがあります。
