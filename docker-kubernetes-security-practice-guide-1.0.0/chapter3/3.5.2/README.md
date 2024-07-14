# **3.5.2**: メモリ使用量を制限する

* `memory-2g.yaml`: KubernetesのPodマニフェスト中で、コンテナが使用できるメモリを2GiBに制限する例 (リスト177) です。
  メモリを大量に使用するワークロードとして、`stress-ng` コマンドを指定しています。
  `kubectl top pod` (テキスト**3.7.5**参照) で確認すると、制限が効いていることがわかります。

```console
$ kubectl top pod
NAME        CPU(cores)   MEMORY(bytes)
memory-2g   1752m        1914Mi
```
