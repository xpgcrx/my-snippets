---
Title: whois
Description: |
  whoisコマンドは、ドメイン名やIPアドレスの登録情報を照会するために使用されます。
  ドメインの所有者、連絡先情報、ネームサーバーなどを確認できます。
Tags:
  - linux
  - network
  - whois
---

### 基本的な使い方

`whois`は引数にドメイン名またはIPアドレスを指定して実行します。

```bash
whois google.com
```

### 出力の見方

`whois`の出力は、照会するドメインのレジストラによって形式が異なりますが、一般的に以下の情報が含まれます。
（プライバシー保護のため、一部の情報は非公開になっている場合があります）

| フィールド                      | 説明                                                                                |
| :------------------------------ | :---------------------------------------------------------------------------------- |
| `Domain Name`                   | ドメイン名。                                                                        |
| `Registry Domain ID`            | レジストリにおけるドメインの一意なID。                                              |
| `Registrar WHOIS Server`        | このドメインのWHOIS情報を提供しているサーバー。                                     |
| `Registrar`                     | ドメインの登録業者（レジストラ）。                                                  |
| `Updated Date`                  | WHOIS情報の最終更新日。                                                             |
| `Creation Date`                 | ドメインの登録日。                                                                  |
| `Registry Expiry Date`          | ドメインの有効期限。                                                                |
| `Name Server`                   | このドメインが使用しているネームサーバー。                                          |
| `Domain Status`                 | ドメインの状態（例: `clientTransferProhibited` は移管が禁止されていることを示す）。 |
| `Registrant/Admin/Tech Contact` | 登録者、管理者、技術担当者の連絡先情報。                                            |
