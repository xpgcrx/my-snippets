---
Title: yum repolist
Description: |
  yumで設定されているリポジトリの一覧を表示する。
Tags:
  - linux
  - yum
  - package-manager
---

```shell
# 有効・無効を問わずすべてのリポジトリを表示
yum repolist all

# 有効なリポジトリだけを表示（enabled無しでもこの挙動）
yum repolist enabled

# 無効になっているリポジトリだけを表示
yum repolist disabled

# リポジトリ設定ファイルを確認する
ls -l /etc/yum.repos.d/
```
