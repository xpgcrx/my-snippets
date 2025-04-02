---
Title: ssh agentに登録する(ssh-add)
Description: |
  ssh agentに登録する。
  ssh-addの引数なしだと、$HOME/.ssh/id_rsaなどに対して実行される（特定の鍵に対して実行したい場合は引数に指定できる）
  ssh-addで以下の様に出る場合はevalで起動する。
  ```shell
  $ ssh-add
  Could not open a connection to your authentication agent.
  $ eval $(ssh-agent) 
  Agent pid 29099
  ```
  ↓のようなパスフレーズの省略にも応用できる
  Enter passphrase for key '/home/jenkins/.ssh/id_rsa’:
Tags:
  - linux
  - ssh
---

```shell
ssh-add
```
