---
Title: teeでファイル書き込みと標準出力/標準エラー出力を同時にする
Description: |
  ファイル書き込みと標準出力/標準エラー出力を同時にする。
Tags:
  - linux
  - process
  - run
---

```shell
your_command 2>&1 | tee output.log
```
