---
title: Nginx学习
excerpt: Nginx学习
date: 2022-5-27 20:08:23
update: 2022-5-27 20:08:23
categories: 
  - Nginx
tags:
  - 技术
---

# Nginx学习

## 一、Nginx反向代理



### 1.配置代理组

```
upstream ssmp {
    server 127.0.0.1:8080;
    server 127.0.0.1:8081;
}
```

### 2.在location中配置proxy_pass

```
location / {
    root   html;
    index  index.html index.htm;

    # Nginx负载均衡配置
    proxy_pass http://ssmp;
}
```

> 参考：https://blog.csdn.net/zxd1435513775/article/details/102508463
>
> 此处的意思为：`nginx `反向代理服务监听 `192.168.17.129`的`80`端口，如果有请求过来，则转到`proxy_pass`配置的对应服务器上，仅此而已。
> 在location下，同时配置root和proxy_pass选项时，两个选项只会二选一执行

示例：

```
...

http {
    ...
    upstream ssmp {
        server 127.0.0.1:8080;
	    server 127.0.0.1:8081;
    }

    server {
        listen       80;
        server_name  localhost;

        #charset koi8-r;

        #access_log  logs/host.access.log  main;

        location / {
            root   html;
            index  index.html index.htm;
            
	        # Nginx负载均衡配置
	        proxy_pass http://ssmp;
        }
	    ...
    }
	...
}

```

## 二、Nginx动静分离

### 1.配置location匹配静态资源

> 参考：https://blog.csdn.net/WangChuan_HHH/article/details/124761892

① 根据文件后缀匹配

```
# 动静分离
location ~* \.(html|css|js|otf|eot|ttf|woff|woff2|svg|jpg|png|gif|swf|flv|wma|wmv|asf|mp3|mp4|mmf|zip|rar|7z)$ {
    root html;
}
```

② 根据目录匹配

同时也要把images文件夹，js文件夹，css文件夹放到nginx文件夹下的html目录里

```
location /css {
    root html;
    index index.html index.htm;
}

location /images {
    root html;
    index index.html index.htm;
}

location /js {
    root html;
    index index.html index.htm;
}
```

③ 使用正则表达式匹配目录

```
location ~*/(js|css|images) {
    root html;
    index index.html index.htm;
}

```

