---
Title: DNS, nslookup
Description: |
  nslookup は、指定したドメイン名やIPアドレスに対するDNSの名前解決を手動で行うためのコマンド。
  DNSサーバーに問い合わせて、ホスト名やIPアドレスの情報を取得する。
  使いやすいが、最近のLinux環境では dig の方が推奨される。
  インタラクティブモードも利用可能（nslookup のみで実行すると対話モードに入る）
Tags:
  - dns
---

```shell
// example.com のIPアドレスを取得
$ nslookup example.com

// IPアドレス 8.8.8.8 に対応するホスト名を取得（逆引き）
$ nslookup 8.8.8.8

// Google Public DNS（8.8.8.8）を使って example.com を解決
$ nslookup example.com 8.8.8.8
```
