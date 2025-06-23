---
Title: Git Remote Cheatsheet
Description: |
  Git remoteの基本的なコマンドと使用方法のチートシート。
Tags:
  - git
---

### リモート表示

```bash
# すべてのリモートリポジトリを一覧表示
git remote

# 詳細情報（URL）を含めて表示
git remote -v

# 特定のリモートの詳細情報を表示
git remote show <remote-name>

# 例：originの詳細を表示
git remote show origin
```

### リモート追加

```bash
# 新しいリモートリポジトリを追加
git remote add <name> <url>

# 例：originとして追加
git remote add origin https://github.com/username/repository.git

# 例：upstreamとして追加（フォークしたリポジトリの元）
git remote add upstream https://github.com/original-owner/repository.git
```

### リモート変更

```bash
# リモートのURLを変更
git remote set-url <name> <new-url>

# 例：HTTPSからSSHに変更
git remote set-url origin git@github.com:username/repository.git

# リモート名を変更
git remote rename <old-name> <new-name>

# 例：originをmainに変更
git remote rename origin main
```

### リモート削除

```bash
# リモートを削除
git remote remove <name>
# または
git remote rm <name>

# 例：upstreamを削除
git remote remove upstream
```

## 注意点

- `git remote add`で追加するのは接続情報のみで、実際のデータは`git fetch`や`git pull`で取得
- リモートURLの変更は、アクセス方法（HTTPS/SSH）の切り替えや、リポジトリ移行時に便利
