---
Title: Git Worktree Cheatsheet
Description: |
  Git worktreeの基本的なコマンドと使用方法のチートシート。
  複数のブランチで同時に作業するための効率的なワークフローを提供。
Tags:
  - git
  - worktree
  - workflow
  - branch
---

## Git Worktreeとは

複数のブランチで同時に作業できるGitの機能。stashやコンテキスト切り替えなしに、独立した作業ディレクトリを作成可能。

## 基本コマンド

### worktree作成

```bash
# 新しいworktreeを作成
git worktree add <path> <branch-name>

# 例：フィーチャー開発用
git worktree add ../project-feature-auth feature/user-authentication

# 例：バグ修正用
git worktree add ../project-bugfix-api hotfix/api-validation

# 例：実験用
git worktree add ../project-experiment-ui experiment/react-upgrade
```

### worktree管理

```bash
# すべてのworktreeを一覧表示
git worktree list

# worktreeの削除
git worktree remove <path>

# 例：マージ後の削除
git worktree remove ../project-feature-auth

# 古いworktree情報をクリーンアップ
git worktree prune
```

### worktree移動

```bash
# worktreeに移動
cd <worktree-path>

# 例
cd ../project-feature-auth
```

## 命名規則

```
../project-<type>-<description>
```

**Type例:**

- `feature` - 新機能開発
- `bugfix` - バグ修正
- `hotfix` - 緊急修正
- `experiment` - 実験的変更
- `refactor` - リファクタリング

## 便利なワークフロー

### 複数タスクの並行作業

```bash
# メイン作業
git worktree add ../project-feature-auth feature/auth

# 緊急バグ修正
git worktree add ../project-hotfix-memory hotfix/memory-leak

# コードレビュー用
git worktree add ../project-review-pr123 pr-123
```

### worktree状況確認

```bash
# すべてのworktreeとブランチ状況
git worktree list --porcelain

# 各worktreeのgit status
for dir in ../project-*; do
  echo "=== $dir ==="
  git -C "$dir" status --short
done
```

## 注意点

- 同じブランチを複数のworktreeでチェックアウトできない
- 削除前に変更をコミット・プッシュする
- `.git/worktrees/`に設定が保存される
- worktreeディレクトリを直接削除せず`git worktree remove`を使用する

