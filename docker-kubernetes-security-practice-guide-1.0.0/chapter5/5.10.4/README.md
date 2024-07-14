# **5.10.4**: etcd に格納するリソースを暗号化する

- `example-encryption-config.yaml`: EncryptionConfigurationファイルの例 (リスト362)
- `encryption-config.yaml`: リソース暗号化の例で紹介したEncryptionConfigファイル (リスト364)
- `enc-test-secret.yaml`: リソース暗号化の例で暗号化対象として紹介したSecretマニフェスト例 (リスト366)

`encryption-config.yaml` ファイル内では共通鍵(`secret`)を設定する必要があります。
事前に以下のコマンドなどで生成したものに置き換えてください。

```
$ head -c 32 /dev/urandom | base6
```
