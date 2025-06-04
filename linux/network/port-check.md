---
Title: Port Check
Description: |
  指定したポートが開いているか確認する。

  lsof (List Open Files) コマンドは、システムが開いているファイルやプロセスに関する情報を表示する。
  ネットワーク接続もファイルとして扱われるため、特定のポートを使用しているプロセスを確認できる
Tags:
  - linux
  - network
---

```bash
# ポート8080が開いているか確認する
# -i: ネットワーク関連のファイルに絞り込む
sudo lsof -i :8080

# Javaアプリケーションで8080をListenしている場合の出力例
# COMMAND   PID         USER   FD   TYPE             DEVICE SIZE/OFF NODE NAME
# java    61400      my_user  213u  IPv6 0x3cd67ea20f1865c2      0t0  TCP *:http-alt (LISTEN)
```
