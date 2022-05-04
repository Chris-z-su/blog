---
title: Oracle
excerpt: 《收获，不止Oracle》
date: 2022-03-26 00:25:00
update: 2022-03-26 00:25:00
tags:
---

# Oracle从入门到放弃

> 《收获，不止Oracle》

## 1.创建表

```sql
CREATE TABLE test(
  id number(20, 0) NOT NULL PRIMARY KEY,
  FieldAA varchar2(64),
  FieldAB varchar2(64),
  flag varchar(2)
);
```

```sql
insert into test values(1, 'a1','b1','D');
insert into test values(2, 'a2','b2','');
insert into test values(3, 'a3','b3','');
insert into test values(4, 'a4','b4','B');
insert into test values(5, 'a5','b5','');
```



## 2. \<> 和 is not null

```sql
SELECT t.* FROM test t;
```

![image-20220326002040694](images/image-20220326002040694.png)

```sql
SELECT t.* FROM test t where t.flag <> 'D' or t.flag is null;
```

![image-20220326001343382](images/image-20220326001343382-16482250866611.png)

```sql
SELECT t.* FROM test t where t.flag <> 'D';
```

![image-20220326002116539](images/image-20220326002116539.png)

## 3.

