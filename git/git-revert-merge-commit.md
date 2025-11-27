---
Title: Git revert merge commit
Description: |
  developにマージ済みの機能をrevertしたいときの手順（ちゃんとPRを作って実施する場合）。

  マージコミットをrevertするには-mオプションが必要。
Tags:
  - xxx
---

1. developからrevert用のブランチを作成する

```bash
git checkout -b revert-xxx
```

2. マージコミットをrevertする

```bash
# マージコミットをrevertする場合は-mオプション(select mainline parent)が要る
# 当該機能をマージ前のdevelopブランチを正としたい場合なので、-m 1とする
git revert -m 1 <commit hash>
```

3. pushする

```bash
git push origin revert-xxx
```

4. GitHubやBitbucketのUIからブランチのページを開きPR作成
