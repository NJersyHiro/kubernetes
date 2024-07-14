# **3.4.2**: ボリュームやbind-mountをread-onlyにする

* `hostpath-read-only.yaml`: KubernetesのPodマニフェスト中で、ホストのrootファイルシステム (`/)`をread-onlyなhostPathボリュームとして `/foo` にマウントする例 (リスト133) です。
  ログを見ると `/foo/this-fails` への書き込みは失敗することがわかります。
  `/foo/tmp/this-may-succeed` への書き込みは、ホストの `/tmp` が `/` とは別のファイルシステムであれば成功し、同一のファイルシステムであれば失敗します。
