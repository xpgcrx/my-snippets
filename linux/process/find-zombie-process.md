---
Title: Find Zombie Process
Description: |
  ゾンビプロセスを見つける。
  STATにZ, 末尾にdefunctと表示されているのがゾンビプロセス。
  ゾンビプロセスとは: プロセスの実態は存在しないが、
  プロセステーブルにエントリが存在する状態を指す。
  通常は、子プロセスの終了のシグナルを親プロセスに通知され、
  親プロセスが子プロセスの後始末をして、ゾンビ状態にならない
Tags:
  - linux
  - process
---

```shell
ps -ef | grep defunct
```
