---
Title: Git Empty Commit
Description: |
  変更がない状態で空のコミットを作成する。
  CI の再実行や、履歴にマーカーを付けたいときに便利。
Tags:
  - git
---

```bash
git commit --allow-empty -m "chore: empty commit (trigger CI)"
```
