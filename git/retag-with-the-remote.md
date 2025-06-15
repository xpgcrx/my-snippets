---
Title: Retag with the Remote
Description: |
  リモートのタグを付け直す。
Tags:
  - git
---

```bash
# リモートのタグを確認
$ git ls-remote --tags

e6c92345dbed32857fc57fcdf6483f455b2feb9a refs/tags/v1.0.1
e586d3c0ffe0168547889450ec57fcdf6483cc8c refs/tags/v1.0.2
1161ae72857fc57fcdf64808f9fda45cdf6483cc refs/tags/v1.0.3

# リモートのv1.0.3を削除
$ git push origin --delete v1.0.3

# ローカルのv1.0.3を削除
$ git tag -d v1.0.3

# HEADにv1.0.3をローカルで改めて付ける
$ git tag v1.0.3

# リモートにv1.0.3をpush
# 先にリモートのタグを削除しておかないとエラーが出るので注意
$ git push origin v1.0.3
```
