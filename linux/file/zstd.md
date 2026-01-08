---
Title: zstd compression and decompression
Description: |
  zstd（Zstandard）を使用したファイルの圧縮と解凍。
  高い圧縮率と高速な動作が特徴の圧縮アルゴリズム。
Tags:
  - linux
  - zstd
  - compression
---

### 基本的な圧縮

```bash
zstd [file]
```

### 基本的な解凍

```bash
zstd -d [file.zst]
# または
unzstd [file.zst]
```

### 元ファイルを削除せずに圧縮・解凍 (-k, --keep)

```bash
zstd -k [file]
zstd -dk [file.zst]
```

### tarと組み合わせてディレクトリを圧縮・解凍

```bash
# 圧縮
tar -I zstd -cvf archive.tar.zst [directory]

# 解凍
tar -I zstd -xvf archive.tar.zst
```
