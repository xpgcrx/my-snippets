---
Title: DNS, dig
Description: |
  dig は、DNSの詳細な問い合わせを行うためのツール。
  nslookup より詳細な情報が得られるため、より高度なDNSの調査に使われる。
  - dig は nslookup より詳細なDNS情報を提供する
  - +short オプションを使うと簡潔な出力にできる（dig example.com +short）
  - DNSキャッシュや再帰問い合わせの仕組みを確認するのに便利
Tags:
  - dns
---

```shell
// example.com の A レコード（IPv4アドレス）を取得
$ dig example.com

// 逆引きDNSの問い合わせ（PTRレコード）
$ dig -x 8.8.8.8

// Google Public DNS に example.com の問い合わせを実施
$ dig @8.8.8.8 example.com

// example.com のメールサーバー情報（MXレコード）
$ dig example.com MX

// example.com に関連するすべてのレコードを取得
$ dig example.com ANY
```
