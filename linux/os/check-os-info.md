---
Title: Check OS Info
Description: |
  OSの情報を確認するコマンド集。
Tags:
  - linux
  - os
---

```shell
// RedHat系のLinux で、RedHatのバージョンを確認
$ cat /etc/redhat-release

// OSを確認
$ cat /etc/os-release

// カーネルのリリース情報を表示
$ uname -r

// 各CPUの情報を表示
$ cat /proc/cpuinfo

// CPUの概要情報を表示
$ lscpu

// CPUアーキテクチャを表示
$ uname -m
```
