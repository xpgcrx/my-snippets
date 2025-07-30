---
title: SQL DML Cheatsheet
description: SQLのDML（データ操作言語）に関するチートシート。
tags: ["sql", "database"]
---

## データの挿入

### 全てのカラムに値を指定

```sql
INSERT INTO table_name
VALUES (value1, value2, value3, ...);
```

### 特定のカラムに値を指定

```sql
INSERT INTO table_name (column1, column2, column3, ...)
VALUES (value1, value2, value3, ...);
```

### 別のテーブルからデータを挿入

```sql
INSERT INTO table1 (column1, column2)
SELECT column3, column4
FROM table2
WHERE condition;
```

## データの更新

### テーブル内のレコードを更新

```sql
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition;
```

**注意:** `WHERE`句を省略すると、テーブル内の全てのレコードが更新される。

## データの削除

### テーブルからレコードを削除

```sql
DELETE FROM table_name
WHERE condition;
```

**注意:** `WHERE`句を省略すると、テーブル内の全てのレコードが削除される。

### テーブルの全レコードを削除（高速）

```sql
-- DDLとして扱われることもある
TRUNCATE TABLE table_name;
```

## データの選択

### 全てのカラムを選択

```sql
SELECT *
FROM table_name;
```

### 特定のカラムを選択

```sql
SELECT column1, column2, ...
FROM table_name;
```

### 重複を除外して選択

```sql
SELECT DISTINCT column_name
FROM table_name;
```

### 条件に一致するレコードを選択

```sql
SELECT column1, column2, ...
FROM table_name
WHERE condition;
```

#### 演算子

| 演算子        | 説明                     |
| :------------ | :----------------------- |
| `=`           | 等しい                   |
| `<>` or `!=`  | 等しくない               |
| `>`           | より大きい               |
| `<`           | より小さい               |
| `>=`          | 以上                     |
| `<=`          | 以下                     |
| `BETWEEN`     | 範囲内                   |
| `LIKE`        | パターンに一致           |
| `IN`          | リスト内のいずれかに一致 |
| `IS NULL`     | NULLである               |
| `IS NOT NULL` | NULLでない               |
| `AND`         | 全ての条件が真           |
| `OR`          | いずれかの条件が真       |
| `NOT`         | 条件を否定               |

### テーブルの結合

#### INNER JOIN

```sql
SELECT columns
FROM table1
INNER JOIN table2 ON table1.column_name = table2.column_name;
```

#### LEFT JOIN (LEFT OUTER JOIN)

```sql
SELECT columns
FROM table1
LEFT JOIN table2 ON table1.column_name = table2.column_name;
```

#### RIGHT JOIN (RIGHT OUTER JOIN)

```sql
SELECT columns
FROM table1
RIGHT JOIN table2 ON table1.column_name = table2.column_name;
```

#### FULL JOIN (FULL OUTER JOIN)

```sql
SELECT columns
FROM table1
FULL JOIN table2 ON table1.column_name = table2.column_name;
```

### グループ化

```sql
SELECT column_name, aggregate_function(column_name)
FROM table_name
WHERE condition
GROUP BY column_name;
```

#### 集計関数

| 関数      | 説明             |
| :-------- | :--------------- |
| `COUNT()` | 行数を数える     |
| `SUM()`   | 合計値を計算する |
| `AVG()`   | 平均値を計算する |
| `MIN()`   | 最小値を求める   |
| `MAX()`   | 最大値を求める   |

### グループ化後の条件指定

```sql
SELECT column_name, aggregate_function(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

### 結果のソート

```sql
SELECT column_name
FROM table_name
ORDER BY column_name ASC|DESC;
```

- `ASC`: 昇順（デフォルト）
- `DESC`: 降順
