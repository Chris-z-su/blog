---
title: Java面试题
excerpt: Java面试题
date: 2022-5-10 23:21:50
update: 2022-5-10 23:21:50
categories: 
  - Java
tags:
  - Java
  - 编程语言
  - 面试
  - 技术
---
# 一、Java基础

## 1) 集合

### (1) 常见的Java集合

集合的顶层接口是Collection（单列集合）和Map（双列集合），

① Collection接口包括List接口、Set接口和Queue接口，

List接口的实现类有：

- ArrayList（数组，排列有序，可重复，查询快、增删慢，线程不安全。使用默认构造器时，jdk7初始容量是10，jdk8初始容量为0，一个空数组，在add()的时候进行数组扩容为10，扩容大小为原来的1.5倍，newCapacity = oldCapacity + (oldCapacity >> 1)  ）
- LinkedList（底层使用双向链表（jdk1.6之前为循环链表，1.7取消了循环），查询慢，增删快（add()、remove()），线程不安全）
- Vector（底层使用数组，排列有序，可重复，查询快，增删慢，线程安全，效率低，默认扩展一倍容量）

Set接口的实现类有：

- HashSet（底层使用Hash表，排列无序，不可重复，存取速度快，内部是HashMap）
  - 子类LinkedHashSet类（采用Hash表存储，使用双向链表记录插入顺序，内部是LinkedHashMap）
- TreeSet（底层使用二叉树实现，排列无序，不可重复，内部是TreeMap的SortedSet）

Queue接口：在两端出入的List，所以也可以用数组或链表来实现



② Map接口的实现类或子接口有：

- HashMap类（底层是Hash表（数组+链表）；线程不安全；允许KV都为null；键不可重复，值可以重复；负载因子0.75，阈值就是 table 容量乘以负载因子；扩容是直接容量变为2倍；key为null，null 的哈希值永远为 0，因此放在 table[0] 的位置）
- HashTable类（底层是Hash表，使用synchronize保证线程安全，KV都不允许为null，键不可重复，值可以重复）
- ConcurrentHashMap类（ConcurrentHashMap结合了HashMap和HashTable的优点，HashTable每次同步都锁住了整个结构，ConcurrentHashMap的锁是细颗粒度的）
- SortedMap接口
  - NavigableMap接口
    - 实现类TreeMap类
- WeekHashMap类



> HashMap详解：https://blog.csdn.net/qq_29051413/article/details/107860264
>
> 



