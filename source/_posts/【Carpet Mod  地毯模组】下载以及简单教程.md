---
title: 【Carpet Mod / 地毯模组】下载以及简单教程
excerpt: 关于Carpet Mod 地毯模组下载以及简单教程
date: 2022-04-22 23:12:39
update: 2022-04-23 17:14:00
tags:
---

# 【Carpet Mod / 地毯模组】下载以及简单教程

[单机游戏 ](https://www.bilibili.com/read/game#rid=6?from=articleDetail)2020-01-31 17:412.4万阅读 · 261喜欢 · 125评论

[![img](https://i1.hdslb.com/bfs/face/4117f2eaee4b89b46e5126af3bc0c4ddc0dd4a50.jpg@96w_96h_1c_1s.webp)](https://space.bilibili.com/89876983)

[Alan_SHIFT](https://space.bilibili.com/89876983)


#  



# "Carpet Mod / 地毯模组" 是用来干什么的？

我个人觉得有用的和常用的就下面这3个：

  \1. 弄一个假人帮你完成一些事情，比如帮你种树

  \2. 可以测试你做的机器的效率，比如帮你测试树场效率

  \3. “子弹时间”，放慢/加快游戏运行速度，可以让玩家更加清晰地观看红石电路时如何运行的





![img](https://i0.hdslb.com/bfs/article/4adb9255ada5b97061e610b682b8636764fe50ed.png@progressive.webp)





# 如何下载 Carpet Mod / 地毯模组

【地毯模组（目前版本为1.3.7），适用于Java版我的世界1.15.2】

\1. 进入网址：

https://github.com/gnembon/fabric-carpet/releases/tag/v1.3-frozen



\2. 在此网页的最下方找到

fabric-carpet-1.15.2-1.3.7+v200127.jar



\3. 单击这个蓝色的名字即可下载（文件大小为：788 KB）



![img](https://i0.hdslb.com/bfs/article/60b9abefdffbba499e1220972ba1942491bed6f4.png@942w_1046h_progressive.webp)鼠标左键单击红色框内的文件

![img](https://i0.hdslb.com/bfs/article/4adb9255ada5b97061e610b682b8636764fe50ed.png@progressive.webp)





# 如何安装mod和使用mod： 

已经有很多很多人都分享了如何安装和使用mod的视频了，请自行去搜索





![img](https://i0.hdslb.com/bfs/article/4adb9255ada5b97061e610b682b8636764fe50ed.png@progressive.webp)





# Carpet Mod 的详细教程视频请观看：

\1. Youtube/油管:

链接：https://youtu.be/Lt-ooRGpLz4

作者：gnembon



\2. 哔哩哔哩：

[bilibili站内链接](https://www.bilibili.com/video/av70188771)

av号：[AV70188771](https://www.bilibili.com/video/av70188771)

搬运者：Aye10032，红石科技搬运组



![img](https://i0.hdslb.com/bfs/article/c3cbbfb94fc77eedc43800b3e7b7c6d7c44591cf.jpg@942w_590h_progressive.webp)原作者的教程的视频封面

![img](https://i0.hdslb.com/bfs/article/4adb9255ada5b97061e610b682b8636764fe50ed.png@progressive.webp)





# 我的世界单位换算：

(Minecraft的循环程序是以每秒20周期的固定速度运行的。因此每刻发生在每0.05秒)

0.1秒 == 1红石刻 == 2游戏刻 == 2 game tick == 2 gt





![img](https://i0.hdslb.com/bfs/article/02db465212d3c374a43c60fa2625cc1caeaab796.png@progressive.webp)

![img](https://i0.hdslb.com/bfs/article/02db465212d3c374a43c60fa2625cc1caeaab796.png@progressive.webp)

![img](https://i0.hdslb.com/bfs/article/02db465212d3c374a43c60fa2625cc1caeaab796.png@progressive.webp)





# ------  指令  ------

# 假人 相关指令：



1) 开启召唤假人的功能：

/carpet commandPlayer true



2) 召唤名为Steve（名字可以自己设置）的假人：

（假人的跟玩家的朝向一致，位置一致，游戏模式一致）

/player Steve spawn

 

3) 让名为Steve的假人持续使用一项物品，例如持续右键

（需要玩家先将物品扔给假人，让假人手持物品）

/player Steve use continuous



4) 让名为Steve的假人持续使用左键

/player Steve attack continuous



5) 让名为Steve的假人使用一项物品，仅使用一次

（需要玩家先将物品扔给假人，让假人手持物品）

/player Steve use



6) 让名为Steve的假人停止一切动作

/player Steve stop



7) 将名为Steve的假人左右手上的物品交换

/player Steve swapHands



8) 移除名为Steve的假人：

/player Steve kill



![img](https://i0.hdslb.com/bfs/article/69355be6160d365303fd30ddd3cfa7867d45d547.png@942w_528h_progressive.webp)在树场的“假人”Steve





![img](https://i0.hdslb.com/bfs/article/db75225feabec8d8b64ee7d3c7165cd639554cbc.png@progressive.webp)





# 计算红石机器效率/漏斗计数 相关指令：



\1) 开启漏斗计数功能：

/carpet hopperCounters true



\2) 开始统计所有对准白色羊毛的漏斗吸收到的物品数量：

（在漏斗对准的地方放羊毛，换成其他16种颜色也行）

/log counter white



\3) 按键盘上的Tab键查看，或者输入下面的指令来查看

/counter white



\4) 根据实际时间计算效率，不是根据游戏内的时间来计算

/counter white realtime



\5) 重置对准所有颜色的羊毛的漏斗的计数：

/counter reset



\6) 重置对准白色羊毛的漏斗的计数：

（或者点击输入/counter white后显示的消息中那个红色的叉叉）

/counter white reset





![img](https://i0.hdslb.com/bfs/article/f0cf9836e1a2aead9723cfb68e02b2db8e635b20.png@942w_530h_progressive.webp)漏斗需要对准羊毛



![img](https://i0.hdslb.com/bfs/article/db75225feabec8d8b64ee7d3c7165cd639554cbc.png@progressive.webp)



# 控制游戏速度/检测物体占用资源 相关指令：



\1) 开启控制游戏速度功能：

/carpet commandTick true



\2) 让游戏在一段时间内以最高速度运行，同时每一游戏刻的计算任务不变

（注意，此命令可以通过加快游戏速度来更快地获得长时间的测试数据）

（72000游戏刻刚好相当于一小时）

/tick warp 72000



\3) 游戏加速结束后，会在左下角给出提示

（例如：24000游戏刻加速结束后，在左下角说：done，提示玩家此次加速结束）

/tick warp 24000 say done



\4) 取消游戏加速

/tick warp



\5) 冻结游戏

（再次输入即可解冻）

/tick freeze



\6) 在冻结游戏的情况下，让游戏运行一小段时间后再次暂停

（例如，让游戏运行2游戏刻，也就是运行0.1秒）

/tick step 2



\7) 调节游戏速度（正常速度为20，可换成其他自然数）：

（“子弹时间”，观看红石电路具体是如何运行的）

/tick rate 20



\8) 检测什么东西占用了游戏资源，无关紧要或者可以忽略的不会显示

（任何资源占用应该小于1游戏刻，也就是50ms，如果大于50ms，说明游戏在掉刻）

/tick health 200



\9) 检测实体占用的游戏资源

（左下角会从大到小给出实体占用资源的排序，可以针对性地减少占用资源多的实体的数量来降低卡顿）

/tick entities



![img](https://i0.hdslb.com/bfs/article/b78c56429ced302dc667e2800ed14504b42cae74.png@942w_498h_progressive.webp)用指令加速游戏时间来测试白桦树场的效率

# 补充:

写这篇专栏的目的就是：

1. 给自己建个“云备忘录”，忘了一些指令打开看看就行
2. 分享dalao做的非常好用的mod/模组的一些常用的用法，毕竟功能和指令有点多
3. 明示下一个视频是关于白桦树场的简单又高效的做法教程（应该会咕好一阵才会出视频吧）



本文为我原创

[ 我的世界 ](https://search.bilibili.com/article?keyword=我的世界&from_source=article)[红石 ](https://search.bilibili.com/article?keyword=红石&from_source=article)[使用方法 ](https://search.bilibili.com/article?keyword=使用方法&from_source=article)[Minecraft ](https://search.bilibili.com/article?keyword=Minecraft&from_source=article)[Carpet Mod](https://search.bilibili.com/article?keyword=Carpet Mod&from_source=article)