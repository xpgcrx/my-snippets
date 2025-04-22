---
Title: Delete unused docker resources
Description: |
  未使用のDockerリソースを一括で削除する。
  特に --volumes オプションを付けることで、未使用のボリューム（永続データ）も削除対象に含まれる
  削除対象になるもの
  - コンテナ: 停止中のもの
  - イメージ: 未使用（どのコンテナにも紐付いてない）
  - ネットワーク: 未使用のカスタムネットワーク
  - ボリューム: どのコンテナからも参照されていないもの（← --volumes が必要）
Tags:
  - docker
---

```shell
docker system prune --volumes
```
