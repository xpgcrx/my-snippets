---
Title: Undo Staging
Description: |
  ステージング取り消し方法。

  restoreに--stagedを付け忘れるとワークツリー内の
  変更自体が失われてしまうので注意。
Tags:
  - git
---

```bash
# 指定したファイルのステージングを取り消す
git restore --staged <file name>

# ディレクトリごと取り消し
git restore --staged <directory name>

# 全部取り消し。
git restore --staged .
# reset版
git reset
```
