# **3.3.1**: 不要なケーパビリティを削除する

* `var_lib_kubelet_config.yaml`: `CAP_NET_RAW` 無しでの `ping` コマンドの実行に必要となる、`net.ipv4.ping_group_range` パラメータを設定するための `KubeletConfiguration` の例 (リスト115) です。
  ファイルパスは通常、`/var/lib/kubelet/config.yaml` です。[Kubernetes 1.18以降では、この設定は不要となる見込みです。](https://github.com/kubernetes/kubernetes/pull/85463)

* `ping-group-range.yaml`: KubernetesのPodマニフェスト中で 、ケーパビリティ無しに `ping` コマンドを実行する例 (リスト116) です。
  Kubernetes 1.18より前のバージョンでは、`var_lib_kubelet_config.yaml` に示す通り、あらかじめ `net.ipv4.ping_group_range` パラメータの設定を許可しておく必要があります。
