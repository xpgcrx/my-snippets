---
title: "Show lines before and after match with grep"
description: "grepでマッチした行の前後N行を合わせて表示する方法。-A (After), -B (Before), -C (Context)オプションを使用する。"
tags:
  - linux
  - grep
---

## After (後)

`grep -A <行数>` で、マッチした行の **後** N行を表示します。

```bash
# マッチした行とその後3行を表示
grep -A 3 'pattern' file.txt
```

## Before (前)

`grep -B <行数>` で、マッチした行の **前** N行を表示します。

```bash
# マッチした行とその前3行を表示
grep -B 3 'pattern' file.txt
```

## Context (前後)

`grep -C <行数>` で、マッチした行の **前後** N行を表示します。
これは `-A <行数> -B <行数>` と同じです。

```bash
# マッチした行とその前後3行を表示
grep -C 3 'pattern' file.txt
```
