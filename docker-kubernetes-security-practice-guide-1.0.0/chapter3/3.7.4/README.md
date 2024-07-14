# **3.7.4**: コンテナの挙動を監視する (auditd)

* `etc_audit_rules.d_foo.rules`: audtdで `/usr/bin` への書き込みを監視するための設定例 (リスト237) です。
  `/etc/audit/rules.d/foo.rules` のようなパスに配置してお使いください。

* `etc_audit_rules.d_cis.rules`: CIS Docker Benchmark version 1.2.0 で監視を推奨されているパスへの書き込みを、auditdで監視するための設定例です。
  ただし、`/var/lib/docker` を除きます。
  `/etc/audit/rules.d/cis.rules` のようなパスに配置してお使いください。
