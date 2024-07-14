# **3.5.1**: CPUコア使用量を制限する

* `cpu-500m.yaml`: KubernetesのPodマニフェスト中で、コンテナが使用できるCPU時間を0.5コア分 (500ミリコア分)に制限する例 (リスト169) です。
  CPUを大量に使用するワークロードとして、`stress-ng` コマンドを指定しています。
  `kubectl top pod` (テキスト**3.7.5**参照) で確認すると、制限が効いていることがわかります。

```console
$ kubectl top pod
NAME       CPU(cores)   MEMORY(bytes)   
cpu-500m   499m         9Mi
```
