---
Title: DNS, getent
Description: |
  getent は、システムのネームサービススイッチ（NSS: Name Service Switch）を介して、
  ホスト名の解決やユーザー情報の取得を行う。
  - nslookup や dig とは異なり、NSSの設定（/etc/nsswitch.conf）に従って名前解決を行う
  - DNSだけでなく、/etc/hosts も利用する
Tags:
  - dns
---

```shell
// /etc/hosts や DNS の情報を参照して example.com のIPアドレスを取得
$ getent hosts example.com

// 8.8.8.8 に対応するホスト名を取得
$ getent hosts 8.8.8.8

// /etc/passwd から username の情報を取得
$ getent passwd username
```
