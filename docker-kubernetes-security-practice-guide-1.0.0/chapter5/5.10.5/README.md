# **5.10.5**: KMSと連携してSecretsを管理する

- `transit-user.hcl`: HashiCorp VaultのTransit Secret Engineに対する権限を割り当てたポリシー例 (リスト368)
- `kms-plugin.yaml`: HashiCorp Vault KMS pluginの設定ファイルの例 (リスト369)
- `encryption-config.yaml`: HashiCorp Vault KMS pluginを有効にしたEncyptionConfigurationファイルの例 (リスト369)
- `kms-plugin-test-secret.yaml`: KMS Pluginを使ったリソース暗号化の例で暗号化対象として紹介したSecretマニフェスト例 (リスト371)

**5.10.5** で紹介している `EncryptionConfiguration` ファイルは **5.10.4** で試したリソース暗号化の内容をそのまま引き継いでいますので、ファイルには**5.10.4** で生成した共通鍵を設定してください。
異なった共通鍵やproviderから該当の項目を除外してしまった場合には過去に暗号化したリソースが復号化できなくなってしまうので注意が必要です。
**5.10.4** の内容を実施していない場合には `EncryptionConfiguration` ファイル内で指定するproviderは `kms` だけでも構いません。

`kms-plugin.yaml`内で設定している値については、実際にHashiCorp Vaultに設定した内容に合わせて適当に変更してください。
