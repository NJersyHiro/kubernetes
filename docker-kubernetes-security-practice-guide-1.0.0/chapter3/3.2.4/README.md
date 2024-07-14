# **3.2.4**: ランタイム自体を非rootで動かす (Rootlessモード)

* `etc_sysctl.conf`: `/etc/sysctl.conf` の設定例です。Ubuntu 18.04やRHEL/CentOS 8.1での利用を想定しています。
  ホスト側のポート番号が1024未満のTCP, UDPポートを公開するためのパラメータ `net.ipv4.ip_unprivileged_port_start` の設定 (リスト109) を含みます。
  また、テキストでは紹介しませんでしたが、pingを許可するためのパラメータ`net.ipv4.ping_group_range` の設定も含んでいます。

* `etc_sysctl.debian.conf`: `etc_sysctl.conf` に、Debian GNU/Linux 9および10向けの設定 (リスト102) を加えたものです。

* `etc_sysctl.el7.conf`: `etc_sysctl.conf` に、RHEL/CentOS 7向けの設定 (リスト102) を加えたものです。
