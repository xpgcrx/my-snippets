---
Title: npm update global packages
Description: |
  npm outdated -g でグローバルパッケージの更新可能一覧を確認し、
  npm update -g ですべてのグローバルパッケージを最新バージョンに更新
Tags:
  - npm
---

```bash
# グローバルパッケージの更新可能一覧を確認
npm outdated -g

# すべてのグローバルパッケージを更新
npm update -g

# 特定のパッケージのみ更新する場合
npm update -g <package-name>
```

