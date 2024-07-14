# **5.10.6**: CSIを利用する

- `csi-test.hcl`: HashiCorp VaultのKV Secrets Engineに対する権限を割り当てたポリシー例 (リスト372)
- `csi-driver.yaml`: Ephemeralボリュームモードを有効にしたCSIDriverのマニフェスト例 (リスト375)
- `secret-provider-class.yaml`: HashiCorp Vaultを外部シークレットストアとして利用するSecretProviderClassのマニフェスト例 (リスト376)
- `secret-via-csi-pod.yaml`: HashiCorp Vaultに格納された秘密情報をCSIを使ってマウントするPodのマニフェスト例 (リスト377)

`SecretProviderClass`ではobjectPathに`/csi-test`、objectNameに`my-secret`を指定していますが、その他roleNameなどを含めて実際にHashiCorp Vaultに設定した内容に合わせて適当に変更してください。
