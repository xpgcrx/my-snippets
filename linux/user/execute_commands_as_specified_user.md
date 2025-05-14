---
Title: Execute a command as a specified user
Description: |
  特定のユーザとしてコマンドを実行する。
  `su`の`-c`オプションを使う。
Tags:
  - linux
  - user
---

```bash
# my-userで"ls -lGh"を実行する例
su - my-user -c "ls -lGh"
```
