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

---

# 例
$ ssh-copy-id test-host
/usr/bin/ssh-copy-id: INFO: Source of key(s) to be installed: ssh-add -L
/usr/bin/ssh-copy-id: INFO: attempting to log in with the new key(s), to filter out any that are already installed
/usr/bin/ssh-copy-id: INFO: 1 key(s) remain to be installed -- if you are prompted now it is to install the new keys
yuki_yoshida@111.222.333.444's password:

Number of key(s) added: 1

Now try logging into the machine, with: "ssh 'test-host'"
and check to make sure that only the key(s) you wanted were added.

$ ssh test-host
```
