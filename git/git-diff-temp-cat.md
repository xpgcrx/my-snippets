---
Title: git diffをデフォルトの形式で出力する
Description: |
  git diffをデフォルトの形式で出力する。
  deltaなどをpagerに設定している場合でもデフォルト形式で出力が可能。
  GitHubのコメントに貼り付けるときなどに便利。
Tags:
  - git
---

```shell
git -c core.pager=cat diff <filepath>
```
