---
title: SpringCloud学习
excerpt: SpringCloud+RabbitMQ+Docker+Redis+搜索+分布式，史上最全面的springcloud微服务技术栈课程|黑马程序员Java微服务,知识分享官,JAVA,黑马程序员,分布式,微服务,spring cloud,微服务架构,ElasticSearch,SpringCloud,科技,计算机技术,哔哩哔哩,Bilibili,B站,弹幕
date: 2022-06-17 12:00:00
update: 2022-06-17 12:00:00
categories: 
  - Java
  - Spring
tags:
  - Java
  - 编程语言
  - 框架
  - 技术
---

# SpringCloud学习

> https://www.kuangstudy.com/course
>
> Dubbo/Zookeeper初识：https://www.kuangstudy.com/course/detail/1321005322055974914
>
> 【黑马程序员】SpringCloud+RabbitMQ+Docker+Redis+搜索+分布式：https://www.bilibili.com/video/BV1LQ4y127n4
>
> 【狂神说Java】SpringCloud最新教程IDEA版：https://www.bilibili.com/video/BV1jJ411S7xr
>
> 参考笔记：https://www.xn2001.com/archives/663.html
>
> 视频资源教程下载：
> https://pan.baidu.com/s/169SFtYEvel44hRJhmFTRTQ
> 提取码：1234
>
> https://www.52pojie.cn/thread-1653246-1-1.html
>
> 百度链接：https://pan.baidu.com/s/1Ez60k6VY4c9IaUExyy2e0Q?pwd=gvw9 提取码：gvw9 

## 一、认识微服务

### 1. 微服务技术栈

![image-20220623170325044](../images/image-20220623170325044.png)

### 2. 微服务架构特征

微服务是一种经过良好架构设计的**分布式**架构方案，微服务架构特征：

- 单一职责：微服务拆分粒度更小，每一个微服务都对应唯一的业务能力，做到单一职责，避免重复业务开发
- 面向服务：微服务对外暴露业务接口
- 自治：团队独立、技术独立、数据独立、部署独立
- 隔离性强：服务调用做好隔离、容错、降级，避免出现级联问题

![image-20220623172517628](../images/image-20220623172517628.png)

### 3. 总结

#### 单体架构特点

- 简单方便，高度耦合，扩展性差，适合小型项目。例如：学生管理系统

#### 分布式架构特点

- 松耦合，扩展性好，但架构复杂，难度大。适合大型互联网项目，例如：京东、淘宝

#### 微服务：一种良好的分布式架构方案

- 优点：拆分粒度更小、服务更独立、耦合度更低
- 缺点：架构非常复杂，运维、监控、部署难度提高

### 4. 微服务结构

微服务这种方案需要技术框架来落地，如SpringCloud和阿里巴巴的Dubbo。

![image-20220623173336331](../images/image-20220623173336331.png)

### 5. 微服务技术对比

![image-20220623173851569](../images/image-20220623173851569.png)

### 6. SpringCloud

- SpringCloud是目前国内使用最广泛的微服务框架。官网地址：https://spring.io/projects/spring-cloud
- SpringCloud集成了各种微服务功能组件，并基于SpringBoot实现了这些组件的自动装配，从而提供了良好的开箱即用体验

![image-20220623174803493](../images/image-20220623174803493.png)

![image-20220623183832199](../images/image-20220623183832199.png)

![image-20220623183906052](../images/image-20220623183906052.png)

![image-20220623183951348](../images/image-20220623183951348.png)

![image-20220623184212744](../images/image-20220623184212744.png)

![image-20220623193925602](../images/image-20220623193925602.png)

![image-20220627192514512](../images/image-20220627192514512.png)

![image-20220627193436114](../images/image-20220627193436114.png)



![image-20220627193734115](../images/image-20220627193734115.png)

![image-20220627193927977](../images/image-20220627193927977.png)



![image-20220627194742191](../images/image-20220627194742191.png)

![image-20220628122331943](../images/image-20220628122331943.png)

![image-20220628123149308](../images/image-20220628123149308.png)

> D:\dev\nacos\bin
>
> PS D:\dev\nacos\bin> .\startup.cmd -m standalone
>
> http://192.168.1.102:8848/nacos/index.html#/login
>
> username: nacos
>
> password: nacos



![image-20220628142329510](../images/image-20220628142329510.png)

![image-20220628142820053](../images/image-20220628142820053.png)

![image-20220628150403684](../images/image-20220628150403684.png)

![image-20220628150823628](../images/image-20220628150823628.png)

![image-20220628160455774](../images/image-20220628160455774.png)

## nacos集群搭建

```shell
# Nginx
PS C:\Users\chris> cd D:\dev\nginx-1.20.2
PS D:\dev\nginx-1.20.2> start .\nginx.exe

# nacos单体
D:\dev\nacos\bin
PS D:\dev\nacos\bin> .\startup.cmd -m standalone

http://192.168.1.102:8848/nacos/index.html#/login
http://169.254.48.182:8848/nacos/index.html


# nacos集群
D:\dev\cluster\nacos1\bin
D:\dev\cluster\nacos2\bin
D:\dev\cluster\nacos3\bin

PS D:\dev\cluster\nacos1\bin> clear
PS D:\dev\cluster\nacos1\bin> .\startup.cmd

# 访问：http://localhost/nacos
# 用户名/密码: nacos/nacos
```





## Nacos集群启动报错：Caused by: java.net.BindException: Address already in use: bind

> https://www.cnblogs.com/liqinzhen/p/12975011.html

```shell
# 解决办法：
#     在命令窗口输入命令：netstat -ano | findstr 8848（8848改成自己被占用的 端口）,
#     然后输入结束进程的命令 ：taskkill /pid 14076 /f  一个一个关掉进程。

PS C:\Users\chris> netstat -ano | findstr 8846
  TCP    127.0.0.1:7850         127.0.0.1:8846         SYN_SENT        61620
PS C:\Users\chris>
PS C:\Users\chris> taskkill /pid 61620 /f
成功: 已终止 PID 为 61620 的进程。
PS C:\Users\chris>
```

![image-20220628235845248](../images/image-20220628235845248.png)

![image-20220629000136933](../images/image-20220629000136933.png)

![image-20220629001130644](../images/image-20220629001130644.png)

![image-20220629002113457](../images/image-20220629002113457.png)

![image-20220629002324934](../images/image-20220629002324934.png)

![image-20220629002448281](../images/image-20220629002448281.png)

![image-20220629110735435](../images/image-20220629110735435.png)

![image-20220629111802254](../images/image-20220629111802254.png)

![image-20220629123311660](../images/image-20220629123311660.png)

![image-20220629123345575](../images/image-20220629123345575.png)

![image-20220629123441500](../images/image-20220629123441500.png)

> 参考文档：
>
> https://docs.spring.io/spring-cloud-gateway/docs/current/reference/html/#gateway-starter
>
> https://docs.spring.io/spring-cloud-gateway/docs/current/reference/html/#the-after-route-predicate-factory
