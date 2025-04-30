---
Title: Conda
Description: |
  Condaコマンド集
Tags:
  - conda
---

```bash
# 環境にインストールされているパッケージの情報を表示
conda list

# Condaのインストール可能パッケージ情報を表示(conda-forgeチャンネルのmacos用のlibgrpcの例)
conda search 'libgrpc[channel=conda-forge, subdir=osx-64]'

# Condaのパッケージ情報を表示(conda-forgeチャンネルのmacos用のlibgrpcの例)
conda search 'libgrpc[channel=conda-forge, subdir=osx-64]' --info
```
