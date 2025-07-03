---
Title: npm global packages cheatsheet
Description: |
  npmのグローバルパッケージを管理する方法
Tags:
  - npm
  - node
---

```bash
# グローバルパッケージの一覧表示（トップレベルのみ）
npm list -g --depth=0

# パッケージをグローバルにインストール
npm install -g <package_name>

# グローバルパッケージをアンインストール
npm uninstall -g <package_name>

# グローバルパッケージの更新可能一覧を確認
npm outdated -g

# 特定のグローバルパッケージをアップデート
npm update -g <package_name>

# 古いグローバルパッケージをすべてアップデート
npm update -g

# グローバルパッケージの場所を表示
npm root -g
```
