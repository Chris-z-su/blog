---
title: redis启动命令
excerpt: redis启动命令
date: 2022-06-13 13:53:26
update: 2022-06-13 13:53:26
categories: 
  - Redis
tags:
  - 技术
  - Linux
---

# redis启动命令

```
[root@10 ~]# redis-server /usr/local/bin/rdconf/redis.conf 
[root@10 ~]# 
[root@10 ~]# systemctl status redis
Unit redis.service could not be found.
[root@10 ~]# fuser -n tcp 6379
6379/tcp:            21168
[root@10 ~]# 
[root@10 ~]# ps -ef|grep redis
root       21168       1  0 09:48 ?        00:00:00 redis-server 127.0.0.1:6379
root       34592    3136  0 09:53 pts/1    00:00:00 grep --color=auto redis
[root@10 ~]# redis-cli
127.0.0.1:6379> ping
PONG
127.0.0.1:6379> 
```

Centos8 开发端口

```
# 新系统中应先判断 firewalld 是否在运行（Centos8 查看服务命令）
systemctl status firewalld
# 开放端口
firewall-cmd --permanent --zone=public --add-port=6379/tcp
# 使规则生效
firewall-cmd --reload
# 查看所有端口
firewall-cmd --list-all
```

