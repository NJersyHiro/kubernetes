# **3.2.1**: ユーザを指定する

* `docker-compose.yaml`: Docker ComposeでUIDを指定する例 (リスト77) です。コンテナで`id` コマンドを実行し、ログにUIDを出力します。

* `Dockerfile.alpine`: Alpine Linux をベースとするDockerfile中でユーザ名を指定する例 (リスト79) です。

* `Dockerfile.ubuntu`: Ubuntu をベースとするDockerfile中でユーザ名を指定する例 (リスト80) です。

* `run-as-user.yaml`: KubernetesのPodマニフェスト中でUIDを指定する例 (リスト82) です。
  Pod内のコンテナで`id` コマンドを実行し、ログにUIDを出力します。 `kubectl logs run-as-user` で確認できます。`kubectl exec -it run-as-user sh` コマンドでシェルに入っても確認できます。

* `run-as-user.deployment.yaml`: KubernetesのDeploymentマニフェスト中でUIDを指定する例 (リスト83) です。
