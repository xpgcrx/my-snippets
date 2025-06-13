---
Title: Maven Cheat Sheet
Description: |
  Javaプロジェクトのライフサイクル管理、依存関係処理、
  ビルド操作に関する重要なMavenコマンド集
Tags:
  - java
  - maven
  - build
  - dependency
---

## プロジェクト作成
```bash
# 新しいMavenプロジェクトを作成
mvn archetype:generate -DgroupId=com.example.app -DartifactId=my-app \
  -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false

# Webアプリケーションを作成
mvn archetype:generate -DgroupId=com.example.webapp -DartifactId=my-webapp \
  -DarchetypeArtifactId=maven-archetype-webapp -DinteractiveMode=false
```

## ビルドライフサイクル
```bash
# プロジェクトをクリーン
mvn clean

# ソースコードをコンパイル
mvn compile

# テストを実行
mvn test

# プロジェクトをパッケージ化（JAR/WARを作成）
mvn package

# ローカルリポジトリにインストール
mvn install

# リモートリポジトリにデプロイ
mvn deploy

# 完全なビルドサイクル（clean + compile + test + package）
mvn clean package

# ビルド時にテストをスキップ
mvn clean package -DskipTests
```

## 依存関係管理
```bash
# 依存関係ツリーを表示
mvn dependency:tree

# 有効なPOMを表示
mvn help:effective-pom

# 依存関係を解決
mvn dependency:resolve

# ソースをダウンロード
mvn dependency:sources

# JavaDocをダウンロード
mvn dependency:resolve -Dclassifier=javadoc

# 依存関係の使用状況を分析
mvn dependency:analyze
```

## プラグイン操作
```bash
# 特定のプラグインゴールを実行
mvn plugin:goal

# Javaメインクラスを実行
mvn exec:java -Dexec.mainClass="com.example.App"

# 引数付きで実行
mvn exec:java -Dexec.mainClass="com.example.App" -Dexec.args="arg1 arg2"

# Spring Bootアプリケーションを実行
mvn spring-boot:run
```

## 情報とヘルプ
```bash
# プロジェクト情報を表示
mvn help:describe -Dplugin=compiler

# 利用可能なプロファイルをリスト表示
mvn help:all-profiles

# 有効な設定を表示
mvn help:effective-settings

# POMを検証
mvn validate
```

## テスト
```bash
# 全てのテストを実行
mvn test

# 特定のテストクラスを実行
mvn test -Dtest=TestClassName

# 特定のテストメソッドを実行
mvn test -Dtest=TestClassName#testMethodName

# パターンでテストを実行
mvn test -Dtest="*TestCase"

# テストレポートを生成
mvn surefire-report:report
```

## 共通オプション
```bash
# 詳細出力
mvn -X clean compile

# 静寂出力（エラーのみ）
mvn -q clean compile

# オフラインモード
mvn -o clean compile

# スナップショットを更新
mvn -U clean compile

# 特定の設定ファイルを使用
mvn -s settings.xml clean compile

# システムプロパティを定義
mvn -Dproperty=value clean compile
```

## プロファイル管理
```bash
# プロファイルを有効化
mvn -Pprofile-name clean compile

# 有効なプロファイルをリスト表示
mvn help:active-profiles

# 複数のプロファイルを有効化
mvn -Pprofile1,profile2 clean compile
```

## リポジトリ操作
```bash
# JARをローカルリポジトリにインストール
mvn install:install-file -Dfile=path/to/file.jar \
  -DgroupId=com.example -DartifactId=example -Dversion=1.0 -Dpackaging=jar

# ローカルリポジトリをクリア
rm -rf ~/.m2/repository

# 依存関係を強制更新
mvn clean compile -U
```