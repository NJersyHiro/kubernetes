# **4.2.1**: BuildKit

* `buildkitd.yaml`: BuildKitのDeploymentマニフェスト例 (リスト264) です。
  テキストでは省略しましたが、`.spec.template.spec.volumes[].secret.secretName` に `ca.pem`、`cert.pem`、`key.pem` を含む Secret を指定してください。
