---
Title: Git Submodule
Description: |
  Git Submodule関連
Tags:
  - git
---

```bash
# submoduleのコードを持ってくる
# submoduleのディレクトリに入って以下を実行
git submodule update --init --recursive

# submodule更新
# リポジトリAがリポジトリBをsubmoduleとしているとする
# リポジトリAのルートディレクトリで以下を実行
# その後差分が検知されるので、addしてcommitする
git submodule update --remote

# git submodule update --remoteを取り消したい場合
# --remoteを外して再度updateを実行する
git submodule update

# update --remoteでcommitされたあとにチェックアウト済みのディレクトリの
# submoduleのディレクトリ内を更新したい時
# git pullでupdate --remoteを取り込んでからupdate
git pull
git submodule update
```
