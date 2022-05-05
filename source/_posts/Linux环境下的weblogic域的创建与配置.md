---
title: Linux环境下的weblogic域的创建与配置
excerpt: Linux环境下的weblogic域的创建与配置，这只是weblogic创建域的一种方式，还可以使用py脚本或者其他脚本执行去创建。
date: 2021-08-03 09:35:36
categories: weblogic
tags: 
  - 中间件
  - 技术
---
## weblogic创建新域
****版本：****
> Java：jdk1.8.0_291
> weblogic：Oracle WebLogic Server 12.2.1.4(fmw_12.2.1.4.0_wls)


*说明：这只是weblogic创建域的一种方式，还可以使用py脚本或者其他脚本执行去创建。这是我创建成功的示例。*

*关于weblogic安装参考*：[Linux环境下weblogic的安装与配置](https://chris-z-su.github.io/2021/08/11/Linux%E7%8E%AF%E5%A2%83%E4%B8%8Bweblogic%E7%9A%84%E5%AE%89%E8%A3%85%E4%B8%8E%E9%85%8D%E7%BD%AE/)

## 一、查看weblogic环境变量

```bash
[weblogic@dcyscxcbap01 bin]$ echo $MW_HOME
/home/weblogic12/wls_12c
```
注意：这里如果查看的是空，是可以的，因为我们还没有配置weblogic环境。配置完成后，再查看一次，如果有表示配置成功。
一定要确认好，我配置的时候环境上有两个版本的weblogic，导致有的时候查看的不一样。修改还是不起作用，以后再研究研究。

1.在（~）路径下设置环境变量
```bash
[weblogic@dcyscxcbap01 ~]$ cat ~/.bashrc 
# .bashrc

# Source global definitions
if [ -f /etc/bashrc ]; then
	. /etc/bashrc
fi

# User specific aliases and functions
[weblogic@dcyscxcbap01 ~]$ 
```

2.设置完执行  source ~/.bashrc 
注意：
①保存的时候提示：
".bashrc" E212: 无法打开并写入文件
解决：需要切换到root用户进行配置:
**su root**

```bash
[weblogic@localhost ~]$ vim ~/.bashrc
# .bashrc

# Source global definitions
if [ -f /etc/bashrc ]; then
	. /etc/bashrc
fi

# User specific aliases and functions
export MW_HOME="/home/weblogic12/wls_12c"
export WL_HOME="/home/weblogic12/wls_12c/oracle_common"
[weblogic@localhost ~]$ source ~/.bashrc
```
②配置完成后，注意切回weblogic用户：su weblogic
查看一下是否配置成功：
```bash
[weblogic@dcyscxcbap01 bin]$ echo $MW_HOME
/home/weblogic12/wls_12c
```
## 二、创建自定义domain的文件夹路径

```bash
[weblogic@localhost ~]$ mkdir -p /home/weblogic12/wls_12c/user_projects/domains/base_domain/
```


进入weblogic中的common的bin目录下

```bash
[weblogic@dcyscxcbap01 bin]$ pwd
/home/weblogic12/wls_12c/wlserver/common/bin
```

## 三、运行wlst.sh开始设置域
下边是设置过程
```bash
[weblogic@dcyscxcbap01 bin]$ ./wlst.sh 
WARNING: This is a deprecated script. Please invoke the wlst.sh script under oracle_common/common/bin.

Initializing WebLogic Scripting Tool (WLST) ...

Welcome to WebLogic Server Administration Scripting Shell

Type help() for help on available commands

wls:/offline> readTemplate('/home/weblogic12/wls_12c/wlserver/common/templates/wls/wls.jar')
警告: readTemplate 已过时。在 selectTemplate 后请使用 loadTemplates 以取代 readTemplate。
wls:/offline/base_domain>cd('Servers/AdminServer')
wls:/offline/base_domain/Server/AdminServer>set('ListenAddress','')
wls:/offline/base_domain/Server/AdminServer>set('ListenPort', 7201)
wls:/offline/base_domain/Server/AdminServer>cd('../..')
wls:/offline/base_domain>cd('Security/base_domain/User/weblogic')
wls:/offline/base_domain/Security/base_domain/User/weblogic>cmo.setPassword('weblogic123')
wls:/offline/base_domain/Security/base_domain/User/weblogic>setOption('OverwriteDomain', 'true')
wls:/offline/base_domain/Security/base_domain/User/weblogic>writeDomain('/home/weblogic12/wls_12c/user_projects/domains/base_domain')
wls:/offline/cpi_domain/Security/cpi_domain/User/weblogic>closeTemplate()
wls:/offline>exit()


Exiting WebLogic Scripting Tool.
[weblogic@dcyscxcbap01 bin]$ 


```
说明：
1.只需要输入 wls:...>后边的命令就行了
2.set('ListenAddress','')  
这个我默认为空，不设置也可以
3.set('ListenPort', 7001)
welogic域监听的端口号，修改成自己想要设置的
4.cmo.setPassword('weblogic123')
设置域的登录密码
5.writeDomain('/home/weblogic12/wls_12c/user_projects/domains/base_domain')
设置上边新建的目录为新建域的工作目录
6.其他的基本是固定


## 四、正常设置完后，可以去base_domain目录下查看，有很多文件，应该是设置成功了

```bash
[weblogic@dcyscxcbap01 bin]$ cd /home/weblogic/wls_12c/user_projects/domains/base_domain/
```

**启动**
方式一：
```bash
[weblogic@dcyscxcbap01 base_domain]$ sh startWebLogic.sh 
```
这样启动后，按ctrl + c , 服务就会停止

方式二(推荐)：
1.将启动日志写入到nohup.out文件中
nohup sh startWebLogic.sh &
```bash
[weblogic@dcyscxcbap01 base_domain]$ pwd
/home/weblogic12/wls_12c/user_projects/domains/base_domain
[weblogic@dcyscxcbap01 base_domain]$ nohup sh startWebLogic.sh &


```
2.ctrl + c  退出，不会停止服务
查看nohup.out文件

```bash
[weblogic@dcyscxcbap01 base_domain]$ tail -1000f nohup.out
```

## 五、查看服务

```bash
[weblogic@dcyscxcbap01 base_domain]$ ps -ef|grep java
```
或者直接根据端口号查找
```bash
[weblogic@dcyscxcbap01 base_domain]$ fuser -n tcp 7201
7201/tcp:             1380
[weblogic@dcyscxcbap01 base_domain]$
```

## 六、停止服务

```bash
[weblogic@dcyscxcbap01 base_domain]$ kill -9 4975 4976
```
或者

```bash
[weblogic@dcyscxcbap01 base_domain]$ kill -9 1380
```


## 七、weblogic域管理控制台地址
http://127.0.0.1:7001/console/
输入设置的用户名 weblogic 密码 weblogic123  即可。

完结！！！有需要再补充吧。
