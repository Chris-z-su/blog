---
title: youtube-dl使用介绍
excerpt: youtube-dl使用介绍
date: 2022-06-13 13:53:26
update: 2022-06-13 13:53:26
categories: 
  - YouTube
tags:
  - 技术
---

# 【备份】youtube-dl使用介绍

[![img](https://upload.jianshu.io/users/upload_avatars/1294473/245972fd-8b0d-484b-abea-44c6cd699b02.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96/format/webp)](https://www.jianshu.com/u/36a21d20d831)

[江南之恋](https://www.jianshu.com/u/36a21d20d831)关注

42019.01.03 21:10:56字数 1,244阅读 136,731

去年12月18日，那篇介绍youtube-dl的文章突然被封，修改申诉未得到任何回复。下面是后台的备份。

------

> https://www.jianshu.com/p/6bae57859325

# 下载安装所需软件

#### Step1 下载与安装Python

1.访问[Python官网](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.python.org%2F)下载最新版本的Python

![img](https://upload-images.jianshu.io/upload_images/1294473-83af12768c40f2c9.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

Python官网


2.安装[Python 3.5.2](https://links.jianshu.com/go?to=https%3A%2F%2Fwww.python.org%2Fftp%2Fpython%2F3.5.2%2Fpython-3.5.2.exe),注意勾选下面的`Add Python 3.5 to PATH`



![img](https://upload-images.jianshu.io/upload_images/1294473-7e7961778136f4ba.png?imageMogr2/auto-orient/strip|imageView2/2/w/670/format/webp)

安装Python

3.按`Win+R`键打开运行，输入`cmd`，再输入`python`并回车执行，如果出现如下界面，则代表安装成功

![img](https://upload-images.jianshu.io/upload_images/1294473-21caa19540d84149.png?imageMogr2/auto-orient/strip|imageView2/2/w/979/format/webp)

Python



#### Step2 安装youtube-dl

- **方式一** 下载Windows exe程序使用
  从[官网](https://links.jianshu.com/go?to=http%3A%2F%2Frg3.github.io%2Fyoutube-dl%2F)下载[youtube-dl.exe](https://links.jianshu.com/go?to=https%3A%2F%2Fyt-dl.org%2Fdownloads%2F2016.10.02%2Fyoutube-dl.exe)然后放在电脑的任意目录下(比如我这里的C:\Users\LOLO)即可使用;可以通过下面的命令来更新youtube-dl

  

  ```undefined
  youtube-dl -U
  ```

- **方式二** 直接使用命令行来安装**（推荐）**
  在安装了Python之后,按`Win+R`键打开运行，输入`cmd`，再输入下面的代码即可自动下载安装youtube-dl

  

  ```cpp
  pip install youtube-dl //直接安装youtube-dl
  pip install --upgrade youtube-dl //安装youtube-dl并更新
  ```

安装完之后,输入`youtube-dl`,如果出现下面的提示,则表明youtube-dl已经安装好啦

![img](https://upload-images.jianshu.io/upload_images/1294473-e766c991e95fe903.png?imageMogr2/auto-orient/strip|imageView2/2/w/979/format/webp)

youtube-dl

#### Step3 安装ffmpeg

[FFmpeg](https://links.jianshu.com/go?to=https%3A%2F%2Fffmpeg.org%2F)主要用来合并视频分段以及对视频重新编码/封装，与youtube-dl配合使用；不是必须的，但建议安装。
1.进入[FFmpeg官网](https://links.jianshu.com/go?to=https%3A%2F%2Fffmpeg.org%2Fdownload.html),进入下载页面,根据自己的操作系统选择下载最新的32位或64位static版本

![img](https://upload-images.jianshu.io/upload_images/1294473-0a76315c2296c2f4.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

选择下面对应的操作系统，比如中间的Windows

![img](https://upload-images.jianshu.io/upload_images/1294473-c40760b1c4a52d63.png?imageMogr2/auto-orient/strip|imageView2/2/w/1200/format/webp)

FFmpeg 64-bit Static

2.下载之后解压出来,将会看到这么一堆文件夹

![img](https://upload-images.jianshu.io/upload_images/1294473-f8599a1ad0fac743.png?imageMogr2/auto-orient/strip|imageView2/2/w/699/format/webp)

FFmpeg

不用管它,直接把这个文件夹改个名字改成"ffmpeg"然后移到C盘根目录

![img](https://upload-images.jianshu.io/upload_images/1294473-5e9fa3d6aa3d09ba.png?imageMogr2/auto-orient/strip|imageView2/2/w/650/format/webp)

FFmpeg

3.打开系统属性>高级系统设置>环境变量

![img](https://upload-images.jianshu.io/upload_images/1294473-be3ee87474a50cc5.png?imageMogr2/auto-orient/strip|imageView2/2/w/1124/format/webp)

环境变量

4.在环境变量>系统变量 里找到Path,点击编辑>新建,然后把刚才那个文件夹里的bin路径(C:\ffmpeg\bin)复制到这里

![img](https://upload-images.jianshu.io/upload_images/1294473-96115f82aa23d76b.png?imageMogr2/auto-orient/strip|imageView2/2/w/1119/format/webp)

添加Path

5.打开Win+R,输入cmd,回车,输入以下命令:



```undefined
ffmpeg -version
```

如果出现如下图所示的版本号信息,则表明FFmpeg安装成功了，你可以在命令提示行中任意文件夹下运行FFmpeg



![img](https://upload-images.jianshu.io/upload_images/1294473-9734296ba4a849b6.png?imageMogr2/auto-orient/strip|imageView2/2/w/979/format/webp)

FFmpeg版本

------

# 代理设置

以SS为例（其他的请自行查阅相关资料，不过多介绍）
开启全局模式之后，无需代理设置，本步骤略过

![img](https://upload-images.jianshu.io/upload_images/1294473-be0d40052e2ef1d8.png?imageMogr2/auto-orient/strip|imageView2/2/w/376/format/webp)

SS全局代理模式

如果用PAC模式，那么后文提到的命令都需要加上这样的代理设置



```cpp
  --proxy "https://127.0.0.1:1080"
  //或者直接这样
  --proxy 127.0.0.1:1080
```

![img](https://upload-images.jianshu.io/upload_images/1294473-75d000f7b4520ca7.png?imageMogr2/auto-orient/strip|imageView2/2/w/977/format/webp)

加上SS代理设置

------

# 下载YouTube视频

- 查看视频所有类型,只看不下载
  `youtube-dl -F [url]`
  或者
  `youtube-dl --list-formats [url]`
  这是一个列清单参数，执行后并不会下载视频，但能知道这个目标视频都有哪些格式存在，这样就可以有选择的下载啦！

![img](https://upload-images.jianshu.io/upload_images/1294473-5c8620972c0957c3.png?imageMogr2/auto-orient/strip|imageView2/2/w/979/format/webp)

查看YouTube视频所有类型

- 下载指定质量的视频和音频并自动合并
  `youtube-dl -f [format code] [url]`
  通过上一步获取到了所有视频格式的清单，最左边一列就是编号对应着不同的格式.
  由于YouTube的1080p及以上的分辨率都是音视频分离的,所以我们需要分别下载视频和音频,可以使用137+140这样的组合.
  如果系统中安装了ffmpeg的话, youtube-dl 会自动合并下下好的视频和音频, 然后自动删除单独的音视频文件

![img](https://upload-images.jianshu.io/upload_images/1294473-5fabdc8817bb3135.png?imageMogr2/auto-orient/strip|imageView2/2/w/979/format/webp)

下载1080p的视频

- 下载字幕
  youtube-dl --write-sub [url] //这样会下载一个vtt格式的英文字幕和mkv格式的1080p视频下来

  

  ```cpp
  youtube-dl --write-sub --skip-download [url] //下载单独的vtt字幕文件,而不会下载视频
  
  youtube-dl --write-sub --all-subs [url] //下载所有语言的字幕(如果有的话)
  
  youtube-dl --write-auto-sub [url] //下载自动生成的字幕(YouTube only)
  ```

![img](https://upload-images.jianshu.io/upload_images/1294473-191ff153e45eea04.png?imageMogr2/auto-orient/strip|imageView2/2/w/979/format/webp)

下载字幕和视频

- 下载视频列表
  youtube-dl -f [format code] [palylist_url] //这种方式可以下载制定清晰度的mp4视频

  

  ```cpp
  youtube-dl [playlist_url] //下载视频列表,这种方式下载的视频可能是mkv格式或者webm格式
  
  youtube-dl -cit [playlist_url] //下载视频列表,这种方式下载的视频可能是mkv格式或者webm格式
  
  youtube-dl --yes-playlist [url] //当链接为视频列表,则下载该列表视频,跟上面的一样,可能是mkv或者webm格式
  ```

------

# 下载Vimeo视频

Vimeo的视频下载起来比较方便,因为没有分离,可以直接下载1080p带音频的视频
命令与下载YouTube的基本一致;下面贴几张图

![img](https://upload-images.jianshu.io/upload_images/1294473-4e1b9f4b18e94700.png?imageMogr2/auto-orient/strip|imageView2/2/w/979/format/webp)

解查看Vimeo视频所有类型

![img](https://upload-images.jianshu.io/upload_images/1294473-5720dba2d2ab972e.png?imageMogr2/auto-orient/strip|imageView2/2/w/979/format/webp)

直接下载Vimeo最高质量视频

------

youtube-dl支持的网站很多,大家可以从作者整理的[这个列表](https://links.jianshu.com/go?to=https%3A%2F%2Frg3.github.io%2Fyoutube-dl%2Fsupportedsites.html)里查看支持的网站(不过由于有的网站接口算法升级,可能当初支持的网站现在不能很好的支持了),如果您要下载的视频网站现在不能用youtube-dl下载的,不妨试试另外一个同样基于Python开发的下载工具You-Get~

> youtube-dl官网：[https://yt-dl.org/](https://links.jianshu.com/go?to=https%3A%2F%2Fyt-dl.org%2F)
> GitHub项目：[https://github.com/rg3/youtube-dl/](https://links.jianshu.com/go?to=https%3A%2F%2Fgithub.com%2Frg3%2Fyoutube-dl%2F)