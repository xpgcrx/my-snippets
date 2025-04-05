---
Title: nohup
Description: |
  SIGHUPを無視する設定でプロセスを起動する。
  nohupで起動したプロセスは、`jobs -l`でPID付きで確認できるので、
    止めるときはkillする。(jobsコマンドは、現在のシェルで実行中のジョブの状態を表示する)
Tags:
  - linux
  - process
  - run
---

```shell
// カレントディレクトリにnohup.outログが出来る
$ nohup <command> &
```
