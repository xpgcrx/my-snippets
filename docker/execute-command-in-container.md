---
title: Execute Command in Docker Container
description: Dockerコンテナ内で指定した単一のbashコマンドを実行する方法。
  ※ bashが使えない軽量コンテナの場合はshかも
tags:
  - docker
  - container
---

```bash
docker exec <container_id_or_name> bash -c "echo 'Hello from container'"
```
