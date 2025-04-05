---
Title: Change file owner/group
Description: |
  ファイルの所有者やグループを変更する。
Tags:
  - linux
  - file
---

```shell
// rootの持ち物になってしまっているものをfugaグループ、hogeユーザの持ち物にする例
// -R: 再帰的に変更
$ sudo chown -R hoge.fuga .

// rootの持ち物になってしまっているimportant.txtファイルをxxxユーザの持ち物に変更する
$ sudo chown xxx: /home/root/important.txt

// カレントディレクトリ以下に対し再帰的にオーナーをxxxユーザに変更
$ sudo chown -R xxx: /home/root/data
```
