---
title: Minecraft CarpetMod常用命令
excerpt: Minecraft CarpetMod常用命令
date: 2022-04-30 17:49:00
update: 2022-04-30 17:49:00
categories: Carpet
tags:
  - Minecraft
  - mod
  - 游戏
---

> wiki：https://github.com/gnembon/fabric-carpet/wiki/Current-Available-Settings

## 1. 显示tps

```shell
/log tps
# 详见  6. log 指令与玩家单独数据
```

## 2. 召唤硅胶人：

开启命令（重启服务器后失效）

```shell
/carpet <特性名> <设定值>
```

### 1) 开启召唤假人的功能：

```shell
/carpet commandPlayer true
```

### 2) 召唤名为Steve（名字可以自己设置）的假人：

（假人的跟玩家的朝向一致，位置一致，游戏模式一致）

```shell
/player Steve spawn
```

```shell
守卫者农场挂机：
/player Steve spawn at 1232 184 1023
女巫塔：
/player Steve spawn at -294 187 -361
/player Steve spawn at -292 187 -361
刷铁塔：
/player Alex spawn at 374.70 63.00 -416.20

#################################################
空置域挂机平台：
中间：
/player Alex spawn at 906 94 -361

空置域中间：
/player kzy01 spawn at 829 100 -377

左边：
/player kzy02 spawn at 887 95 -439

右边：
/player Steve spawn at 872 99 -300

/player kzy03 spawn at 770 97 -303
/player kzy04 spawn at 770 95 -439
/player kzy05 spawn at 766 95 -377
#################################################

```


### 3) 让名为Steve的假人持续使用一项物品，例如持续右键

（需要玩家先将物品扔给假人，让假人手持物品）

```shell
/player Steve use continuous
```

### 4) 让名为Steve的假人持续使用左键

```shell
/player Steve attack continuous
```

### 5) 让名为Steve的假人使用一项物品，仅使用一次

（需要玩家先将物品扔给假人，让假人手持物品）

```shell
/player Steve use
```

### 6) 让名为Steve的假人停止一切动作

```shell
/player Steve stop
```

### 7) 将名为Steve的假人左右手上的物品交换

```shell
/player Steve swapHands
```

### 8) 移除名为Steve的假人：

```shell
/player Steve kill
```

### 7) 让假人扔出东西

```shell
# 扔出手上的东西
/player kzy02 drop
```



### 99) 说明

```shell
控制玩家
可以对玩家进行相应的操控,无论是真玩家还是"硅胶小人"(假玩家),又或者是你自己,这些行为是在服务器运行,在操控自己时,自己可能看不到相应的UI,但别的玩家可以看到

player <name> <option>

name  指定玩家名
option  选项
	once #一次
	continuous #持续
	interval #间隔
	forward #前方
	east #东方
	spawn
		在玩家所在位置生成一个"硅胶小人"且游戏模式相同,若该玩家名存在,则该玩家上线时会顶替掉硅胶小人
	drop
		让硅胶小人把手持的物品丢出来
	mount
		让硅胶小人坐在附近的实体上
	dismount
		让硅胶小人从实体上下来
	look <方向>
		让硅胶小人朝向相应方向
	move <方向>
	stop
		停止硅胶小人所有动作
	swapHands
		交换主手和副手上的物品
	use <选项>
		使用,相当于右键
	attack <选项>
		攻击相当于左键, 选项同use
	shadow
		会让同名硅胶小人顶替真实玩家的位置(真实玩家下线),并完成你之前给他们的任务,只能在服务器使用,单机下线内置服务端会关闭 
作者：worldy丶jj https://www.bilibili.com/read/cv5948362/ 出处：bilibili
```

## 3. 切换模式命令

观察者模式带"夜视"和"海豚的恩惠"效果

```shell
carper commandCameramode true
/c /s 快速切换 观察者/生存 模式
给普通玩家使用/c, /s权限,可以快速切换观察者/生存模式
```

> 作者：worldy丶jj https://www.bilibili.com/read/cv5948362/ 出处：bilibili

F3 + P：开启或关闭Minecraft失去窗口焦点时的自动暂停功能。

**命令格式：/gamemode <模式> [<目标>]**

**<模式>：survival（生存模式）、creative（创造模式）、adventure（冒险模式）、spectator（旁观模式）**

1、“gamemode0”生存模式。

2、“gamemode1”创造模式。

3、“gamemode2”冒险模式。

4、“gamemode 3”旁观模式。

## 4. 单个玩家睡觉跳过夜晚

字面意思

 ```shell
 carpet onePlayerSleeping true
 ```

> 作者：worldy丶jj https://www.bilibili.com/read/cv5948362/ 出处：bilibili



1.17版本以后的单人睡觉是gamerule里面的playersleepingprecentage value（value表示百分之多少玩家睡觉跳过晚上，数值范围是0-100）



1.17为什么没有onePlayerSleeping指令呢

2021-09-25 23:24回复

[![img](https://i1.hdslb.com/bfs/face/7e2f6e0d8aabdb749313435344fc13df6ed2b2cd.jpg@96w_96h_1c_1s.webp)](https://space.bilibili.com/38562793)

[凿壁蹭_WIFI](https://space.bilibili.com/38562793)[![img](https://s1.hdslb.com/bfs/seed/jinkela/commentpc/static/img/ic_user%20level_6.64b9440.svg)](https://www.bilibili.com/blackboard/help.html#会员等级相关)改了，在gamerule里面



https://www.sohu.com/a/165552096_114885

很简单，只要使用F3+P,F3+P是一个可以取消切出游戏换面时弹出的ESC游戏选项的功能，也就是说切出游戏不需要打开背包或者打开对话窗即可直接切出，单机玩家不会进入暂停界面。



## 5. 追踪实体信息(村民) track

1.   开启命令：

```shell
/carpet commandTrackAI true
[11:04:29] [Server thread/INFO]: commandTrackAI: true, [change permanently?]
```

2. 使用

```shell
# 显示
/track villager breeding

# 清除
/track villager clear
```

## 6. log 指令与玩家单独数据

更加直接,连续,给每个玩家提供信息,log是根据玩家登陆信息,基于每个玩家的,基于carpet精神,不侵犯原版玩家数据,在服务器重启或重进世界后,玩家log信息会销毁

log <选项>

​	选项

​	tps

​		在tab界面显示服务器卡顿情况TPS,MSPT

​	counter [颜色]

​		能够简洁,连续的显示计数器物品的速度的实时效率

​	mobcaps

​		会持续显示刷怪上限信息

​	pathfinding <值>

​		能用粒子效果显示生物需要<值>毫秒以上完成的所有寻路尝试

​	packets

​		显示服务器端进出数据包的总数量

​	tnt

​		追踪世界中任何tnt实体,初始位置和爆炸位置

​	projectiles

​		追踪抛射物的每一刻的位置

​	fallingBlock

​		追踪实体方块的每一刻的位置 

> 作者：worldy丶jj https://www.bilibili.com/read/cv5948362/ 出处：bilibili

## 7. carpet配置文件
对于服务器管理员 - 手动地配置carpet mod并让地毯指令在游戏中无法调用

carpet.conf

#关闭所有carpet指令,可以在后面启用你需要的特性,玩家进入游戏后,看不到任何carpet指令和特性,除非你在下面开启 

locked

#例如下面的特性开启 

scriptsAutoload true 

renewableCoral true 

> 作者：worldy丶jj https://www.bilibili.com/read/cv5948362/ 出处：bilibili

## 8. 查看所有命令：

```shell
/carpet list default
[09:48:05] [Server thread/INFO]: Carpet Mod Settings matching "default":
[09:48:05] [Server thread/INFO]: - defaultLoggers [none] [tps] [mobcaps,tps]
```

```shell
/carpet list
[09:51:31] [Server thread/INFO]: All Carpet Mod Settings:
[09:51:31] [Server thread/INFO]: - allowSpawningOfflinePlayers [true] [false]
[09:51:31] [Server thread/INFO]: - antiCheatDisabled [true] [false]
[09:51:31] [Server thread/INFO]: - carpetCommandPermissionLevel [ops] [2] [4]
[09:51:31] [Server thread/INFO]: - carpets [true] [false]
[09:51:31] [Server thread/INFO]: - chainStone [true] [false] [stick_to_all]
[09:51:31] [Server thread/INFO]: - cleanLogs [true] [false]
[09:51:31] [Server thread/INFO]: - commandDistance [true] [false] [ops]
[09:51:31] [Server thread/INFO]: - commandDraw [true] [false] [ops]
[09:51:31] [Server thread/INFO]: - commandInfo [true] [false] [ops]
[09:51:31] [Server thread/INFO]: - commandLog [true] [false] [ops]
[09:51:31] [Server thread/INFO]: - commandPerimeterInfo [true] [false] [ops]
[09:51:31] [Server thread/INFO]: - commandPlayer [true] [false] [ops]
[09:51:31] [Server thread/INFO]: - commandProfile [true] [false] [ops]
[09:51:31] [Server thread/INFO]: - commandScript [true] [false] [ops]
[09:51:31] [Server thread/INFO]: - commandScriptACE [ops] [0] [1] [2] [3] [4]
[09:51:31] [Server thread/INFO]: - commandSpawn [true] [false] [ops]
[09:51:31] [Server thread/INFO]: - commandTick [true] [false] [ops]
[09:51:31] [Server thread/INFO]: - commandTrackAI [true] [false] [ops]
[09:51:31] [Server thread/INFO]: - creativeFlyDrag [0.09]
[09:51:31] [Server thread/INFO]: - creativeFlySpeed [1.0]
[09:51:31] [Server thread/INFO]: - creativeNoClip [true] [false]
[09:51:31] [Server thread/INFO]: - creativePlayersLoadChunks [true] [false]
[09:51:31] [Server thread/INFO]: - ctrlQCraftingFix [true] [false]
[09:51:31] [Server thread/INFO]: - customMOTD [_]
[09:51:31] [Server thread/INFO]: - defaultLoggers [none] [tps] [mobcaps,tps]
[09:51:31] [Server thread/INFO]: - desertShrubs [true] [false]
[09:51:31] [Server thread/INFO]: - explosionNoBlockDamage [true] [false]
[09:51:31] [Server thread/INFO]: - extremeBehaviours [true] [false]
[09:51:31] [Server thread/INFO]: - fastRedstoneDust [true] [false]
[09:51:31] [Server thread/INFO]: - fillLimit [32768] [250000] [1000000]
[09:51:31] [Server thread/INFO]: - fillUpdates [true] [false]
[09:51:31] [Server thread/INFO]: - flatWorldStructureSpawning [true] [false]
[09:51:31] [Server thread/INFO]: - flippinCactus [true] [false]
[09:51:31] [Server thread/INFO]: - fogOff [true] [false]
[09:51:31] [Server thread/INFO]: - forceloadLimit [256]
[09:51:31] [Server thread/INFO]: - hardcodeTNTangle [-1] [-1.0]
[09:51:31] [Server thread/INFO]: - hopperCounters [true] [false]
[09:51:31] [Server thread/INFO]: - huskSpawningInTemples [true] [false]
[09:51:31] [Server thread/INFO]: - interactionUpdates [true] [false]
[09:51:31] [Server thread/INFO]: - lagFreeSpawning [true] [false]
[09:51:31] [Server thread/INFO]: - language [none] [zh_cn] [zh_tw]
[09:51:31] [Server thread/INFO]: - leadFix [true] [false]
[09:51:31] [Server thread/INFO]: - lightEngineMaxBatchSize [5] [50] [100] [200]
[09:51:31] [Server thread/INFO]: - lightningKillsDropsFix [true] [false]
[09:51:31] [Server thread/INFO]: - liquidDamageDisabled [true] [false]
[09:51:31] [Server thread/INFO]: - maxEntityCollisions [0] [1] [20]
[09:51:31] [Server thread/INFO]: - mergeTNT [true] [false]
[09:51:31] [Server thread/INFO]: - missingTools [true] [false]
[09:51:31] [Server thread/INFO]: - movableAmethyst [true] [false]
[09:51:31] [Server thread/INFO]: - movableBlockEntities [true] [false]
[09:51:31] [Server thread/INFO]: - optimizedTNT [true] [false]
[09:51:31] [Server thread/INFO]: - perfPermissionLevel [2] [4]
[09:51:31] [Server thread/INFO]: - persistentParrots [true] [false]
[09:51:31] [Server thread/INFO]: - piglinsSpawningInBastions [true] [false]
[09:51:31] [Server thread/INFO]: - pingPlayerListLimit [0] [12] [20] [40]
[09:51:31] [Server thread/INFO]: - placementRotationFix [true] [false]
[09:51:31] [Server thread/INFO]: - portalCreativeDelay [1] [40] [80] [72000]
[09:51:31] [Server thread/INFO]: - portalSurvivalDelay [1] [40] [80] [72000]
[09:51:31] [Server thread/INFO]: - pushLimit [10] [12] [14] [100]
[09:51:31] [Server thread/INFO]: - quasiConnectivity [true] [false]
[09:51:31] [Server thread/INFO]: - railPowerLimit [9] [15] [30]
[09:51:31] [Server thread/INFO]: - renewableBlackstone [true] [false]
[09:51:31] [Server thread/INFO]: - renewableCoral [false] [expanded] [true]
[09:51:31] [Server thread/INFO]: - renewableDeepslate [true] [false]
[09:51:31] [Server thread/INFO]: - renewableSponges [true] [false]
[09:51:31] [Server thread/INFO]: - rotatorBlock [true] [false]
[09:51:31] [Server thread/INFO]: - scriptsAppStore [gnembon/scarpet/contents/programs]
[09:51:31] [Server thread/INFO]: - scriptsAutoload [true] [false]
[09:51:31] [Server thread/INFO]: - scriptsDebugging [true] [false]
[09:51:31] [Server thread/INFO]: - scriptsOptimization [true] [false]
[09:51:31] [Server thread/INFO]: - shulkerSpawningInEndCities [true] [false]
[09:51:31] [Server thread/INFO]: - silverFishDropGravel [true] [false]
[09:51:31] [Server thread/INFO]: - simulationDistance [0] [12] [16] [32]
[09:51:31] [Server thread/INFO]: - smoothClientAnimations [true] [false]
[09:51:31] [Server thread/INFO]: - spawnChunksSize [0] [11]
[09:51:31] [Server thread/INFO]: - stackableShulkerBoxes [false] [true] [16]
[09:51:31] [Server thread/INFO]: - structureBlockIgnored [minecraft:structure_void] [minecraft:air]
[09:51:31] [Server thread/INFO]: - structureBlockLimit [48] [96] [192] [256]
[09:51:31] [Server thread/INFO]: - structureBlockOutlineDistance [96] [192] [2048]
[09:51:31] [Server thread/INFO]: - summonNaturalLightning [true] [false]
[09:51:31] [Server thread/INFO]: - superSecretSetting [true] [false]
[09:51:31] [Server thread/INFO]: - tntDoNotUpdate [true] [false]
[09:51:31] [Server thread/INFO]: - tntPrimerMomentumRemoved [true] [false]
[09:51:31] [Server thread/INFO]: - tntRandomRange [-1] [-1.0]
[09:51:31] [Server thread/INFO]: - updateSuppressionBlock [false] [true] [1] [6]
[09:51:31] [Server thread/INFO]: - updateSuppressionCrashFix [true] [false]
[09:51:31] [Server thread/INFO]: - viewDistance [0] [12] [16] [32]
[09:51:31] [Server thread/INFO]: - xpNoCooldown [true] [false]
```

## 9.forge.mod
https://www.curseforge.com/
https://www.curseforge.com/minecraft/mc-mods/malilib

安装教程：https://www.bilibili.com/video/BV1cX4y1T7RZ

Minecraft我的世界1.18.2Fabric客户端整合包：
https://www.bilibili.com/read/cv15963596/

