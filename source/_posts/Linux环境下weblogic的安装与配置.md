---
title: Linux环境下weblogic的安装与配置
excerpt: Linux环境下weblogic的安装与配置，基于weblogic12 + jdk1.8。
date: 2021-08-11 14:06:48
tags:
---
# 前言

****版本：****
> Java：jdk1.8.0_291
> weblogic：Oracle WebLogic Server 12.2.1.4(fmw_12.2.1.4.0_wls)

****下载地址：****
jdk:

>https://www.oracle.com/java/technologies/java-se-glance.htm

weblogic:
> https://www.oracle.com/middleware/technologies/weblogic-server-downloads.htm

相关资料：

> 「weblogic」https://www.aliyundrive.com/s/HQx6SURUaoa 提取码: 0x8p
> 点击链接保存，或者复制本段内容，打开「阿里云盘」APP ，无需下载极速在线查看，视频原画倍速播放。

# 一、安装jdk
## 1) 上传jdk到任意目录下
```bash
[root@localhost wollo]# pwd
/usr/local/wollo
[root@localhost wollo]# ll
-rw-r--r--. 1 root root 144935989 7月  17 09:33 jdk-8u291-linux-x64.tar.gz
[root@localhost wollo]# 
```

## 2) 解压
```bash
[root@localhost wollo]# tar -xzvf jdk-8u291-linux-x64.tar.gz
```

## 3) 移动安装目录
```bash
[root@localhost wollo]# mv jdk1.8.0_291 /usr/local/
```

## 4) 配置环境变量
```bash
[root@localhost wollo]# vim /etc/profile
#export PATH USER LOGNAME MAIL HOSTNAME HISTSIZE HISTCONTROL
export JAVA_HOME=/usr/local/jdk1.8.0_291
export PATH=$JAVA_HOME/bin:$PATH
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar
[root@localhost wollo]# source /etc/profile

```

## 5) 查看Java版本，验证是否安装成功
```bash
[root@localhost wollo]# Java -version
```

> 附：查看jdk
> 1.whereis java
> 2.which java （java执行路径）


附：我安装jdk1.6、jdk1.7后，使用Java -version命令，发现报错了：
```
[root@10 jdk1.6]# java -version
Error occurred during initialization of VM
Unable to load native library: libnsl.so.1: cannot open shared object file: No such file or directory
```
解决：
执行以下命令：
```
yum install libnsl
```
参考：https://blog.csdn.net/star_star_91/article/details/109395530


# 二、安装weblogic
## 1.创建及配置用户信息

```bash
1.创建用户目录
[root@192 ~]# mkdir -p /home/weblogic

2.创建用户
[root@192 ~]# groupadd weblogic

3.给目录home最大权限
[root@192 ~]# chmod 777 /home

4.添加组
[root@192 ~]# useradd -g weblogic -d /home/weblogic/ weblogic

5.设置密码
[root@192 ~]# passwd weblogic  
用户名：weblogic  
密码：5E4TmUzv

6.赋权限
[root@192 ~]# chown -R weblogic:weblogic /home

7.切换用户
[root@192 ~]# su weblogic
```

## 2.准备
### 1）创建oraInventory目录
```bash
[weblogic@dcyscxcbap01 /]# mkdir /home/oraInventory
```

### 2) 创建weblogic安装目录
```bash
[weblogic@dcyscxcbap01 /]# mkdir /home/weblogic12
```

### 3）配置文件目录

```bash
[weblogic@dcyscxcbap01 /]# mkdir /home/install
[weblogic@dcyscxcbap01 /]# cd /home/install
```
#### a.  上传fmw_12.2.1.4.0_wls.jar到install目录

```bash
[weblogic@dcyscxcbap01 install]$ ll
总用量 846428
-rwxr-xr-x. 1 weblogic weblogic 866733871 7月  17 10:13 fmw_12.2.1.4.0_wls.jar
[weblogic@dcyscxcbap01 install]$
```

#### b.  新建oraInst.loc文件

```bash
[weblogic@dcyscxcbap01 install]$ vim oraInst.loc 
inventory_loc=/home/oraInventory
inst_group=weblogic
```


#### c.  新建wls12c.resp文件

```bash
[weblogic@dcyscxcbap01 install]$ vim wls12c.resp

[ENGINE]

#DO NOT CHANGE THIS.
Response File Version=1.0.0.0.0

[GENERIC]

#Set this to true if you wish to skip software updates
DECLINE_AUTO_UPDATES=true

#My Oracle Support User Name
MOS_USERNAME=

#My Oracle Support Password
MOS_PASSWORD=<SECURE VALUE>

#If the Software updates are already downloaded and available on your local system, then specify the path to the directory where these patches are available and set SPECIFY_DOWNLOAD_LOCATION to true
AUTO_UPDATES_LOCATION=

#Proxy Server Name to connect to My Oracle Support
SOFTWARE_UPDATES_PROXY_SERVER=

#Proxy Server Port
SOFTWARE_UPDATES_PROXY_PORT=

#Proxy Server Username
SOFTWARE_UPDATES_PROXY_USER=

#Proxy Server Password
SOFTWARE_UPDATES_PROXY_PASSWORD=<SECURE VALUE>

#The oracle home location. This can be an existing Oracle Home or a new Oracle Home
ORACLE_HOME=/home/weblogic12/wls_12c

#Set this variable value to the Installation Type selected. e.g. WebLogic Server, Coherence, Complete with Examples.
INSTALL_TYPE=WebLogic Server

#Provide the My Oracle Support Username. If you wish to ignore Oracle Configuration Manager configuration provide empty string for user name.
MYORACLESUPPORT_USERNAME=

#Provide the My Oracle Support Password
MYORACLESUPPORT_PASSWORD=<SECURE VALUE>

#Set this to true if you wish to decline the security updates. Setting this to true and providing empty string for My Oracle Support username will ignore the Oracle Configuration Manager configuration
DECLINE_SECURITY_UPDATES=true

#Set this to true if My Oracle Support Password is specified
SECURITY_UPDATES_VIA_MYORACLESUPPORT=false

#Provide the Proxy Host
PROXY_HOST=

#Provide the Proxy Port
PROXY_PORT=

#Provide the Proxy Username
PROXY_USER=

#Provide the Proxy Password
PROXY_PWD=<SECURE VALUE>

#Type String (URL format) Indicates the OCM Repeater URL which should be of the format [scheme[Http/Https]]://[repeater host]:[repeater port]
COLLECTOR_SUPPORTHUB_URL=

```

## 3.安装

```bash
[weblogic@dcyscxcbap01 install]$ ll
总用量 846428
-rwxr-xr-x. 1 weblogic weblogic 866733871 7月  17 10:13 fmw_12.2.1.4.0_wls.jar
-rwxr-xr-x. 1 weblogic weblogic        62 7月  17 10:15 oraInst.loc
-rwxr-xr-x. 1 weblogic weblogic      1928 7月  17 16:24 wls12c.resp
[weblogic@dcyscxcbap01 install]$ java -jar fmw_12.2.1.4.0_wls.jar -silent -responseFile /home/install/wls12c.resp -invPtrLoc /home/install/oraInst.loc
启动程序日志文件为/tmp/OraInstall2021-07-17_04-38-00PM/launcher2021-07-17_04-38-00PM.log。
正在提取安装程序... . . . 完成
检查 CPU 速度是否大于 300 MHz。   实际为 2419.200 MHz    通过
检查交换空间: 必须大于 512 MB。   实际为 1639 MB    通过
检查此平台是否需要 64 位 JVM。   实际为64    通过 (不需要 64 位)
检查临时空间: 必须大于 300 MB。   实际为 3437 MB    通过
准备从/tmp/OraInstall2021-07-17_04-38-00PM启动 Oracle Universal Installer
日志:/tmp/OraInstall2021-07-17_04-38-00PM/install2021-07-17_04-38-00PM.log
版权所有 (c) 1996, 2019, Oracle 和/或其关联公司。保留所有权利。
正在读取响应文件...
跳过软件更新
开始检查: CertifiedVersions
预期的结果: oracle-6, oracle-7, redhat-7, redhat-6, SuSE-11, SuSE-12, SuSE-15之一
实际结果: redhat-null
检查完成。此次检查的总体结果为: 通过
CertifiedVersions 检查: 成功。


开始检查: CheckJDKVersion
预期的结果: 1.8.0_191
实际结果: 1.8.0_291
检查完成。此次检查的总体结果为: 通过
CheckJDKVersion 检查: 成功。


已启用此会话的验证。
正在验证数据
复制文件
完成百分比: 10
完成百分比: 20
完成百分比: 30
完成百分比: 40
完成百分比: 50
完成百分比: 60
完成百分比: 70
完成百分比: 80
完成百分比: 90
完成百分比: 100

Oracle Fusion Middleware 12c WebLogic Server 和 Coherence 12.2.1.4.0 的 安装 已成功完成。
日志已成功复制到/home/oraInventory/logs。
[weblogic@dcyscxcbap01 install]$ 
```

# 三、weblogic域安装与配置：

> [Linux环境下的weblogic域的创建与配置](https://chris-z-su.github.io/2021/08/03/Linux%E7%8E%AF%E5%A2%83%E4%B8%8B%E7%9A%84weblogic%E5%9F%9F%E7%9A%84%E5%88%9B%E5%BB%BA%E4%B8%8E%E9%85%8D%E7%BD%AE/)
