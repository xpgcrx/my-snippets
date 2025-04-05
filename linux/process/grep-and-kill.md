---
Title: Grep and Kill Process
Description: |
  grepでヒットしたプロセスを全てkillする。
Tags:
  - linux
  - process
---

```shell
ps -ef | grep 'something' | grep -v grep | awk '{print $2}' | xargs kill
```
