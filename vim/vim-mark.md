---
Title: Vim Marks
Description: |
  How to use marks in Vim.
Tags:
  - vim
---

```text
# 現在のカーソル位置をマークする (aはマーク名)
ma

# マークした位置に移動する
`a

# マークした行の先頭に移動する
'a

# マークの一覧を表示する
:marks

# 指定したマークを削除する (aとbを削除する例)
:delmarks a b

# すべてのマークを削除する
:delmarks!
```
