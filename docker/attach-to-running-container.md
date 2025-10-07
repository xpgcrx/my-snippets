---
title: Attach to a Running Container
description: 実行中のDockerコンテナにアタッチして、インタラクティブなシェルセッションを開始する方法。
tags:
  - docker
  - container
---

`-i` (`--interactive`) はコンテナの標準入力を開いたままにし、`-t` (`--tty`) は疑似ターミナルを割り当てる。
この2つのオプションを組み合わせることで、インタラクティブなシェル操作が可能になる

```bash
docker exec -it <container_id_or_name> /bin/bash
```

Alpineなど、bashがインストールされていない軽量なイメージの場合は、代わりに `/bin/sh` を使用する。

```bash
docker exec -it <container_id_or_name> /bin/sh
```
