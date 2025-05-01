---
Title: yum cache
Description: |
  yumのキャッシュまわり
Tags:
  - linux
  - yum
---

```bash
# リポジトリ設定を変更した後や、キャッシュの破損が疑われる場合は以下を実行。
sudo yum clean all # キャッシュの削除。ディスク容量の確保やエラー解消時に使用
sudo yum makecache # リポジトリメタデータの事前取得。yum の動作を高速化
```
