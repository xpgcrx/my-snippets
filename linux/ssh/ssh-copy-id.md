---
Title: ssh-copy-id
Description: |
  リモートホストのauthorized_keysに自分の公開鍵を追加する
Tags:
  - ssh
---

```bash
ssh-copy-id <remote-host>

# 上記を実行後はパスワードを使わず公開鍵認証でssh接続出来る
ssh <remote-host>
```
