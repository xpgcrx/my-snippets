---
title: Stop all running Docker containers
description: 現在実行中のすべてのDockerコンテナを停止します。
tags:
  - docker
---

```bash
docker stop $(docker ps -q)
```
