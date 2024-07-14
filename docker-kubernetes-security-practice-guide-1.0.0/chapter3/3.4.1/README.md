# **3.4.1**: ファイルシステムをread-onlyにする

* `read-only.yaml`: KubernetesのPodマニフェスト中で、rootファイルシステムをread-onlyにし、書き込み可能なtmpfsを `/tmp` にマウントする例 (リスト128) です。
  ログを見ると `/this-fails` への書き込みは失敗し、`/tmp/this-succeeds` への書き込みは成功することがわかります。
