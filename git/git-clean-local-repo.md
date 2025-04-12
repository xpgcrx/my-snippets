---
Title: Git Clean Local Repo
Description: |
  ローカルのGitリポジトリをcheckout直後のまっさらな状態に戻す。
  - -f: 強制的に削除（force）
  - -d: ディレクトリも含めて削除
  - -x: .gitignoreで指定されたファイルも削除

  git clean -nfdで、DryRunもできる。
Tags:
  - git
---

```bash
git clean -fdx
```
