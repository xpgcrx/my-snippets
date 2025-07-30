---
title: SQL DDL Cheatsheet
description: SQLのDDL（データ定義言語）に関するチートシート。
tags: ["sql", "database"]
---

## データベース

### データベースの作成

```sql
CREATE DATABASE database_name;
```

### データベースの削除

```sql
DROP DATABASE database_name;
```

## テーブル

### テーブルの作成

```sql
CREATE TABLE table_name (
    column1 datatype constraint,
    column2 datatype constraint,
    ...
);
```

#### 使用例

```sql
CREATE TABLE employees (
    id INT PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    email VARCHAR(100) UNIQUE,
    hire_date DATE,
    salary DECIMAL(10, 2) CHECK (salary > 0)
);
```

### テーブルの削除

```sql
DROP TABLE table_name;
```

### テーブルの変更

#### カラムの追加

```sql
ALTER TABLE table_name
ADD column_name datatype;

-- INT型のNOT NULLのカラム追加例
ALTER TABLE table_name
ADD COLUMN column_name INT NOT NULL;
```

#### カラムの削除

```sql
ALTER TABLE table_name
DROP COLUMN column_name;
```

#### カラム名の変更

```sql
-- MySQL, MariaDB
ALTER TABLE table_name
RENAME COLUMN old_name TO new_name;

-- PostgreSQL
ALTER TABLE table_name
RENAME COLUMN old_name TO new_name;

-- SQL Server
EXEC sp_rename 'table_name.old_name', 'new_name', 'COLUMN';
```

#### カラムのデータ型変更

```sql
-- MySQL, MariaDB
ALTER TABLE table_name
MODIFY COLUMN column_name new_datatype;

-- PostgreSQL
ALTER TABLE table_name
ALTER COLUMN column_name TYPE new_datatype;

-- SQL Server
ALTER TABLE table_name
ALTER COLUMN column_name new_datatype;
```

#### 制約の追加

##### PRIMARY KEY

```sql
ALTER TABLE table_name
ADD CONSTRAINT pk_constraint_name PRIMARY KEY (column1, column2);
```

##### FOREIGN KEY

```sql
ALTER TABLE table_name
ADD CONSTRAINT fk_constraint_name FOREIGN KEY (column_name) REFERENCES other_table(other_column_name);
```

##### UNIQUE

```sql
ALTER TABLE table_name
ADD CONSTRAINT uq_constraint_name UNIQUE (column_name);
```

##### CHECK

```sql
ALTER TABLE table_name
ADD CONSTRAINT chk_constraint_name CHECK (condition);
```

#### 制約の削除

```sql
-- MySQL, MariaDB
ALTER TABLE table_name
DROP PRIMARY KEY; -- 主キーの場合

ALTER TABLE table_name
DROP FOREIGN KEY fk_constraint_name; -- 外部キーの場合

ALTER TABLE table_name
DROP INDEX uq_constraint_name; -- UNIQUE制約の場合

-- PostgreSQL, SQL Server
ALTER TABLE table_name
DROP CONSTRAINT constraint_name;
```

## インデックス

### インデックスの作成

```sql
CREATE INDEX index_name
ON table_name (column1, column2, ...);
```

### インデックスの削除

```sql
-- MySQL, MariaDB
DROP INDEX index_name ON table_name;

-- PostgreSQL, SQL Server
DROP INDEX index_name;
```

## ビュー

### ビューの作成

```sql
CREATE VIEW view_name AS
SELECT column1, column_name2
FROM table_name
WHERE condition;
```

### ビューの削除

```sql
DROP VIEW view_name;
```
