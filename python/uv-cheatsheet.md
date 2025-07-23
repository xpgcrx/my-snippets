---
Title: uv Cheat Sheet
Description: |
  高速なPythonパッケージインストーラー＆リゾルバーである`uv`のチートシートです。
Tags:
  - python
  - uv
  - packaging
---

```bash
# プロジェクトの初期化
# Python 3.13.2 を使うプロジェクトとして初期化します
uv init -p 3.13.2

# --- Pythonの管理 ---

# インストール可能なPythonバージョンの一覧を表示
uv python list

# Pythonのインストール
uv python install 3.13

# プロジェクトで使うPythonのバージョンを固定 (.python-versionを書き換えます)
uv python pin 3.13.2

# --- 仮想環境 ---

# 仮想環境の作成 (.venvディレクトリが作成されます)
uv venv

# 仮想環境のアクティベート (macOS/Linux)
source .venv/bin/activate

# 仮想環境の状態をuv.lockの内容に同期
uv sync

# --- 依存ライブラリの管理 ---

# パッケージの追加 (pyproject.tomlとuv.lockも更新されます)
uv add requests

# バージョンを指定して追加
uv add 'requests==2.31.0'

# 開発用の依存として追加
uv add moto --dev

# requirements.txtから依存関係を追加
uv add -r requirements.txt

# パッケージの更新
uv add requests --upgrade

# パッケージの削除
uv remove requests

# 開発用の依存を削除
uv remove moto --dev

# --- Pythonの実行 ---

# 管理された仮想環境でスクリプトを実行
uv run main.py

# Pythonバージョンを指定してスクリプトを実行
uv run --python 3.10 example.py

# unittestを実行
uv run python -m unittest test/unit/test_main.py

# --- ツールの実行とインストール ---

# ツールをインストールせずに一時的に実行
uvx ruff check

# バージョンを指定してツールを実行
uvx ruff@0.3.0 check

# ツールを永続的にインストール
uv tool install ruff

# インストール済みのツールを更新
uv tool upgrade ruff

# --- pip互換コマンド ---

# パッケージのインストール
uv pip install requests

# 複数パッケージのインストール
uv pip install "requests>2.0" httpx

# requirements.txtからのインストール
uv pip install -r requirements.txt

# パッケージのアンインストール
uv pip uninstall requests

# インストール済みパッケージの一覧表示
uv pip list

# requirements.txtの生成
uv pip freeze > requirements.txt

# インストール済みパッケージの詳細表示
uv pip show requests

# キャッシュのクリーン
uv cache clean
```

