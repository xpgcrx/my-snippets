---
Title: Check top memory processes with ps
Description: |
  psコマンドを使ってメモリを多く使っているプロセスを上位から確認する
Tags:
  - linux
  - process
  - memory
---

```shell
ps aux --sort=-%mem | head
```
