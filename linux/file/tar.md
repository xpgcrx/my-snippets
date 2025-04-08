---
Title: tar圧縮/解凍
Description: |
  tarは「Tape Archive」の略で、ファイルやディレクトリをアーカイブするためのコマンド。
  - z: gzip 圧縮を使用する。これにより、アーカイブが圧縮され、ディスクスペースを節約できる
  - c: これは「create」の略で、新しいアーカイブを作成する
  - v: 「verbose」の略で、処理中に詳細な情報を表示する。これにより、アーカイブされている各ファイルの名前などが表示される
  - f: これは「file」の略で、次に続く名前（この場合は hoge.tgz）をアーカイブファイルの名前として使用する
  - x: アーカイブを展開する(解凍)
Tags:
  - linux
  - file
---

```bash
// 圧縮
tar zcvf hoge.tgz hoge

// 解凍
tar zxvf hoge.tgz
```
