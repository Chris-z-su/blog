---
title: Minecraft Carpet Mod 命令使用教程
excerpt: Minecraft Carpet Mod 命令使用教程
date: 2022-04-23 15:06:39
update: 2022-04-23 15:06:39
tags:
---

# Minecraft Carpet Mod 命令使用教程

[单机游戏 ](https://www.bilibili.com/read/game#rid=6?from=articleDetail)2020-05-06 23:351.6万阅读 · 203喜欢 · 28评论

[![img](https://i1.hdslb.com/bfs/face/c99358d2c0d25c158090f3bb0fe63cf51b0c1a4b.jpg@96w_96h_1c_1s.webp)](https://space.bilibili.com/7514269)

[worldy丶jj](https://space.bilibili.com/7514269)

粉丝：33   文章：2    关注

Minecraft CarpetMod command use

worldy根据[【MC|熟肉】Carpet Mod（1.14/1.15）详尽教程【gnembon】](https://www.bilibili.com/video/BV1hE411D7um)视频整理

## 什么是carpet

> carpet是对游戏进行了一些魔改,让你能更好的控制游戏内容,并且能更好的理解发生了什么. 移除了游戏中一些烦人的bug/特性,提高了游戏的运行效率,在不影响游戏正常运行的情况下，提供了一些可选的游戏特性或者原版特性缺少的内容. carpet依附于fabric api
>
> 最重要的是,无论你做了什么,游戏依然完全兼容原版.如果你不需要使用这些工具也可以随时关闭,而且不产生任何副作用.

- 使用carpet第一次进入world 游戏特性和原版完全一致,所有特性/bug默认都是关闭的,每个特性需要分别开启才能生效
- 默认开启的只有这些carpet的指令,除非你使用了他们,否则不会产生任何效果,这些指令也可以被关闭,如果你的server管理员想这样做的话

## 如何运用 carpet 指令来配置carpet mod

- 想要开启某个特性,你需要使用carpet指令开启,输入`/carpet <特性名> <设定值>`会暂时改变相应的特性直到重启服务器/重新进入世界

  > (后续本文中将会忽略前面的斜杠"/")

- 临时设置特性后文本框会出现一个链接,点击这个链接,他会给你一个命令,可以设置特性默认开启`/carpet setDefault <特性名> <设定值>`

- 获取所有carpet特性只需要输入`/carpet`

  > 不仅能获得目前激活的特性,也会获得一个可以点击的特性目录,鼠标悬停在上面,可以获得每个指令的具体作用,点击右边的值便可以设置它

- `/carpet list default`显示永久性的设置,就是重启后也会保持的特性

- `/carpet removeDefault`可以删除默认列表中的内容,让他每次重启后都是默认原版的特性

- `/carpet list <关键词>`搜索某项特性,可以通过类别,子字符串方式搜索

- carpet所有指令都是低授权等级的,所有玩家都能使用,管理员可以使用`/carpet setting`指令关闭,设置每个人的权限

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



## 游戏控制

### 游戏tick控制

 tick <选项>

> 控制游戏运行速度,监视资源占用

- <选项>

- - warp [值] [其他指令]

    > 可以让游戏在一定gt内以最高速度运行,同时每个gt内计算任务量不变
    >
    > 可以再该命令后再加一个指令,他会在加速结束后执行
    >
    > 在前一个加速指令完成前不能调用新的warp指令,停止当前加速,只需要把<值>设置成"0"或者不填写<值>

  - `freeze`

    > 冻结gt,使游戏部分暂停,如:计算实体,世界树种,方块事件和更新,允许玩家移动,在冻结状态下研究发生了什么
    >
    > 再次使用该指令可以解除冻结,手动打指令,不能使用命令方块

  - `step`

    > 步进,允许游戏以可控的方式前进,以方便观察变化较快的装置

  - superHot

    > 一个很有趣的指令,在玩家不移动时冻结游戏,只有在玩家移动时时间才会流逝

  - rate [值]

    > 改变游戏的基础时钟,更直接控制游戏速度,在加速与暂停上没有warp/freeze好用,但是他对游戏的影响最小,why?其他方法可能会不是很完美,因为游戏在设计时没有计划应对这种情况,而使用哪个rate就完全和游戏原本的计划相同,只是快慢的区别
    >
    > 时间变慢后客户端动画还是原来的速度你可以开启`carpet smoothClientAnimation true` 这会平滑并放慢客户端渲染,使适配低速度,但是这会使玩家移动和控制变慢,观察活塞运动方便?!

  - health [值]

    > 检测计算资源占用,类似于一个内置的检测器,检查什么东西占用资源
    >
    > 默认检测5s/200gt中的数据,时长可以通过[值]控制
    >
    > 汇总每个gt,每个维度中某样东西平均占用的计算时长,包括网络,自动存档,tick外任务,刷怪,区块加载,区块卸载,方块更新,实体运算,方块实体运算,村民和袭击,环境,如果上述未出现在结果里,说明占用较少,都被归类的到rest(其他)内,你的1gt应该低于50ms,如果比这个长,说明你的游戏已经在掉tick了

  - entities

    > 因为消耗性能的主要问题来源于实体和方块实体,运行一轮只记录实体和方块实体的用时
    >
    > 需要详细情况可以使用原版的debug指令

## 实体生成spawn 指令

> 这些改变不在`carpet`指令下只是暂时的,只需要重启游戏就可以恢复

 spawn <选项>

- 选项

  > 将默认的"70怪/玩家" 改成我们想要的数字使用`set <值>`

  > 选项:reset,重置为原版默认刷怪概率

- - `start`

  - `stop`

  - `monster`

    > 显示一些近期的刷怪记录

  - `mocking`

    > 禁止刷怪,但是这个指令还是会持续尝试刷怪     

  - `tracking [选项] [x1] [y1] [z1] [x2] [y2] [z2]`

    > 刷怪追踪,需要不少的CPU算力,在你正在追踪时直接使用`tracking`也可以显示数据

  - 选项

  - `test`

    > 重置当前刷怪追踪，开始新的追踪，重置漏斗计数

  - `rates <选项> [值]`

    > 更改相应怪物刷出概率

  - 类型

  - `monster`

  - `creature`

    > 列出所有占用刷怪上限的怪物的位置

  - `list <x> <y> <z>`

    > 允许查看我位置可以生成的怪物
    >
    > 不可以省略后面的坐标,光标指向的位置可能会被实体阻挡,导致输出结果不准确,可以使用相对位置 "~ ~ ~"
    >
    > 也可以直接在要检查的位置放置粉色地毯,和无地毯指令的效果一致

  - `entities <类型>`

  - `mobcaps [选项]`

    > 按照大类显示刷怪上限,以及这个类别中检测到了多少只怪
    >
    > 默认显示玩家所在维度刷怪上限,维度:`overworld` , `the_nether` , `the_end`

## 禁用出生点区块

> false禁止出生点区块加载

 carpet disableSpawnChunks false

## 视距调整

> 单机无效,单机可以在选项里自行调节,通常不重启服务器无法调节视距
>
> 使用这个可以再不重启服务器的情况下调节视距

 carpet viewDistance <值>

## Super secret setting

> 超级秘密设置,你问他是干什么的?都说了是秘密了,所以记住,不要开启,不要开启,不要开启.

 catpet superSecretSetting true



## 游戏监控

### 漏斗计数器

> 用于物品计数,将漏斗指向羊毛,漏斗会向羊毛输出物品,羊毛会销毁接受物品并计数
>
> 羊毛的颜色表示用于计数的频道,所有指向同一种颜色羊毛的漏斗会一起计数

 carpet hopperCounters true

> 显示所有计数器

 counter [颜色] [选项]

- 选项

- - `realtime`

    > 根据实际时间计算出效率,而不是游戏时钟

  - `reset`

    > 重置计数器,或重置指定颜色的计数器,输出文本框有红色[x]也可以重置计数

## distance 指令

> 计算

 distance <选项>

- `from <x1> <y1> <z1> to <x2> <y2> <z2>`

  > 给出两个位置之间相距多少米
  >
  > 欧氏距离(Spherical)球面距离或者说直线距离
  >
  > 圆柱距离(Cylindrical)也就是不考虑y轴的直线距离
  >
  > 曼哈顿距离(Manhattan)计程车距离或者说链接两个点需要多少个方块

- `to <x> <y> <z>`

  > 多次计算不同位置到初始点的距离

## info 指令

> 给出方块的信息,之前也提供实体信息,但是在1.14以后加入了`/data`后就不需要了

 info block <x> <y> <z>



## 追踪实体信息(村民) track

> 追踪显示实体信息(目前只有村民实体)

 track <实体> <信息>

- <实体>

- - `villager`

    > 指定村民实体

- <信息>

- - `breeding`

    > 显示村民是否绑定床,食物数量,繁殖冷却
    >
    > 绿宝石右键实体-->显示床
    >
    > 腐肉-->清空实体持有食物
    >
    > 床-->显示实体周围能识别的床

  - `iron_golem_spawning`

    > 铁傀儡生成相关信息,是否睡过觉,工作状态,恐慌状态,最后一次看到铁傀儡时间

  - `clear`

    > 清除显示的信息

# bugFix

# 马游荡修复

> 修复:马会尝试寻路到启程开始的位置,目前不太完善,某些情况可能失效

 carpet horseWanderingFix true

# 栓绳消失修复

> 修复:在加载栓绳绑着动物的区块时,栓绳不正常消失/出现

 carpet leadFix true

# 合成物品快捷键(CTRL + Q)丢弃无效修复

> 使用快捷键可以丢出所有本次合成物品

 carpet ctrlQCraftingFix true

# 地狱门窒息修复

> 地狱门传送实体时会根据实体碰撞箱大小调整地狱门大小,防止实体窒息

# 挖掘幽灵方块修复 (仅1.14)

> 修复1.14 出现烦人的幽灵方块,无论是原版客户端连接carpet server 还是相反情况都有效,1.15原版已修复该bug

 carpet miningGhostBlockFix true

# 优化

# 流畅红石线

> 对红石线更新系统的重新实现,大幅减少红石线亮/灭带来的卡顿

 carpet fastRandstoneDust true

# 实体碰撞上限

> 能够解决很多实体卡在一个地方造成的卡顿
>
> 设置数值较低时会改变大群生物之间的碰撞效果

 carpet maxEntityCollisions [<value>]

# 无卡顿刷怪

> 能够减少刷怪所需算力,优化碰撞计算,实际怪物生成的代码,他不会对原版的刷怪产生任何影响和改动,只是效率更高而已

 carper lagFreeSpawning true

# 地狱门缓存(1.15无此项)

> 修复了如果地狱门15s内没有用过会产生巨大的瞬时卡顿问题,开启后地狱门会永久缓存直到地狱门发生变化
>
> 1.15无此项,因为Mojang使用兴趣点(poi)系统重写了地狱门连接

 carper portalCaching true

# 创造工具

# 控制玩家

> 可以对玩家进行相应的操控,无论是真玩家还是"硅胶小人"(假玩家),又或者是你自己,这些行为是在服务器运行,在操控自己时,自己可能看不到相应的UI,但别的玩家可以看到

 player <name> <option>

- name

  > 指定玩家名

- option

- - 选项

  - `once` #一次

  - `continuous` #持续

  - `interval` #间隔

  - `forward` #前方

  - `east` #东方

  - `spawn`

    > 在玩家所在位置生成一个"硅胶小人"且游戏模式相同,若该玩家名存在,则该玩家上线时会顶替掉硅胶小人

  - `drop`

    > 让硅胶小人把手持的物品丢出来

  - `mount`

    > 让硅胶小人坐在附近的实体上

  - `dismount`

    > 让硅胶小人从实体上下来

  - `look <方向>`

    > 让硅胶小人朝向相应方向

  - `move <方向>`

  - `stop`

    > 停止硅胶小人所有动作

  - `swapHands`

    > 交换主手和副手上的物品

  - `use <选项>`

    > 使用,相当于右键

- `attack <选项>`

  > 攻击相当于左键

- - 选项同`use`

- `shadow`

  > 会让同名硅胶小人顶替真实玩家的位置(真实玩家下线),并完成你之前给他们的任务,只能在服务器使用,单机下线内置服务端会关闭

# 按照形状快速放置

> 目前只支持球形,方形可以用原版指令"fill"填充,或者"replace"替换,对于更复杂的形状推荐使用"script fill"

 draw <形状> <x> <y> <z> <r>

- 形状

- - `sphere`

# 原版fill和cone指令填充上限

> 原版fill只能填充32768个方块,也就相当于32*32*32

 carpet fillLimit [<vanlue>]

# fill/clone/setblock/structure 指令的禁止方块更新

> false禁止指令放置方块时更新

 carpet fillUpdates false

# 活塞推动上限

> 可以自定义活塞推动的上限,但是这会让你的装置其他人用不了

 carpet pushLimit <值>



# 铁轨激活距离上限

> 可以设置充能铁轨的激活上限

 carpet railPowerLimit <值>



# QC开关

> 可以开关QC连接,和BUD激活,false关闭QC

 carpet quasiConnectivity false



# 召唤闪电

> 允许使用`summon`指令生自然成闪电,就像雷雨天气闪电一样,有概率生成骷髅马

 carpet summonNaturalLightning true



# 创造模式地狱门延迟

> 无论什么游戏模式都需要一定时间才能进入地狱门,防止创造模式下传送错维度,开启后手持黑曜石的玩家延迟会更长

 carpet portalCreativeDelay true



# （TNT）爆炸不破坏方块

> 让tnt爆炸不会造成任何方块破坏

 carpet explosionNoBlockDamage true



# TNT放置时不更新

> 防止玩家防止tnt是造成更新

 carpet tntDoNotUpdate true



# 移除TNT的初始随机动量

> 移除点燃tnt时的随机跳动,但是再把装置发给别人之前要确保装置能够处理这种情况

 carpet tntPrimerMomentumRemoved true



# 移除经验球吸取的冷却

> 移除玩家获取经验需要2gt的冷却

 carpet xpNoCooldown true



# 生存工具

# 经验球合并

> 让经验像物品一样,可以合并成更大的经验球

 carpet combineXPOrbs true



# “仙人掌”翻转工具

> 手上拿着仙人掌右键你想要改变朝向的方块,你可以旋转或者翻转它,使用仙人掌不会造成方块更新
>
> 仙人掌放在副手,可以以相反的方向放置方块
>
> 用仙人掌右键沙子"当当"你就种上了一颗仙人掌

 carpet flippinCactus true



# /c /s 快速切换 观察者/生存 模式

> 给普通玩家使用`/c`, `/s`权限,可以快速切换观察者/生存模式
>
> 观察者模式带"夜视"和"海豚的恩惠"效果

 carper commandCameramode true



# 禁用飞行和骑乘的服务器反作弊检测

> 开启后防止因为快速飞行和移动或者连接不稳定,造成回弹,但是不能修复你的连接不稳定

 carpet antiCheatDisable true



# 单个玩家睡觉跳过夜晚

> 字面意思

 carpet onePlayerSleeping true



# 自定义登陆界面服务器欢迎语

> 能够在服务器运行时改变登陆界面服务器欢迎语,不需要关闭服务器修改配置文件

 carpet customMOTD <字符串>



# 缺失的挖掘工具

> 添加活塞，玻璃挖掘工具镐子,海绵的挖掘工具剪刀

 carpet missingTools true



# 发射器旋转方块

> 发射器被激活时能够旋转发射器前面的方块

 carpet rotatorBlock true



# 可移动方块实体 (箱子, 漏斗, 酿造台, 发射器, 信标, etc.)

> 可以移动 箱子, 漏斗, 酿造台, 发射器, 信标, etc.带有nbt数据的方块

 carpet movableBlockEntities true



# 蠹虫破坏方块掉落沙砾

> 在蠹虫离开石头时会掉落砂砾物品

 carpet silverFishDropGravel true



# 尸壳在沙漠神殿中生成

> 开启后沙漠神殿只会刷尸壳,而且不需要露天就能刷

 carpet huskSpawningInTemples true



# 末地城生成潜影贝

> 开启后允许潜影贝在末地城结构范围内刷出

carpet SpawningInEndCities true



# 空潜影箱可堆叠

> 空的潜影盒丢到地上使其合并,然后再捡起来便可,但是其特性仍是不可堆叠的物品

carpet stackableShulkerBoxes true



# “固定”的鹦鹉

> 可以让鹦鹉固定在你的肩膀上,跳跃,骑马,飞行都无法掉下来,只有在水中或者玩家受伤,才能使鹦鹉从肩膀上掉下来

carpet persistentParrots true



# 海带生长高度限制

> 海带生长高度限制,使海带不能过分疯长,但是不适用于玩家放置的海带

carpet kelpGenerationGrowthLimit <值>



# 在干旱的气候中树苗变成枯木

> 在干燥的群系中不能吸收到水分的树苗将会变成枯木

carpet desertShrubs true



# 骨粉催熟珊瑚块

> 开启后可以在水下通过珊瑚植物催熟珊瑚块,和树苗到树的原理是一样的,用骨粉

carpet renewableCoral true



# 闪电将守卫者转变为远古守卫者

> 闪电将守卫者转变为远古守卫者来获取海绵

carpet renewableSponges true



# 其他功能

# 地毯相应的快捷方式

> 这个mod名字的由来?
>
> 开启后能够使用放置不同颜色地毯的方式来执行特定重复的指令
>
> 粉色地毯:`spawn list`检查某个方块刷怪情况
>
> 黑色地毯:`spawn mobcaps`显示刷怪上限,放在不同颜色的羊毛上显示这个类别所有被加载的实体,对应指令:`spawn entities <类型>`
>
> 棕色地毯:`distance <选项>`按住shift或首次放置地毯会设置初始点,而正常放置会设定第二个,从而获得测量结果
>
> 灰色地毯:`info block`提供下方方块信息
>
> 绿色地毯:`counter [颜色]`显示对应频道计数器信息
>
> 红色地毯:`counter [颜色] reset`重置这些计数器

carpet carpets true



# log 指令与玩家单独数据

> 更加直接,连续,给每个玩家提供信息,log是根据玩家登陆信息,基于每个玩家的,基于carpet精神,不侵犯原版玩家数据,在服务器重启或重进世界后,玩家log信息会销毁

log <选项>

- 选项

- - `tps`

    > 在tab界面显示服务器卡顿情况TPS,MSPT

  - `counter [颜色]`

    > 能够简洁,连续的显示计数器物品的速度的实时效率

  - mobcaps

    > 会持续显示刷怪上限信息

  - pathfinding <值>

    > 能用粒子效果显示生物需要<值>毫秒以上完成的所有寻路尝试

  - packets

    > 显示服务器端进出数据包的总数量

  - tnt

    > 追踪世界中任何tnt实体,初始位置和爆炸位置

  - projectiles

    > 追踪抛射物的每一刻的位置

  - fallingBlock

    > 追踪实体方块的每一刻的位置

# 一个好用的计算器

> 什么这个能当计算器使用?好东西!
>
> 其实这是Scarpet的api,Scarpet是carpet游戏内编程工具,允许你运行自定义脚本,在不添加MOD的情况下添加游戏的额外特性

script run 1+1

# 一些在早期版本中存在的功能

# 在世界中生成游戏结构

script run plop(x,y,z,'end_city') #生成末地城



# 来改变群系

script scan x1 y1 z1 x2 y2 z2 x y z set_biome(_,'swamp') 

script run set_biome(x,y,z,'swamp') #改变生物群系为沼泽

# 补充

> Carpet扩展Mod (carpet extra mod)包含一些非原版但是仍然非常酷的功能, 例如自动合成台、发射器放置方块、甚至发射器更多的功能

如何安装carpet mod

> (提示：只需遵循fabric mod设置说明)

# carpet配置文件

> 对于服务器管理员 - 手动地配置carpet mod并让地毯指令在游戏中无法调用

carpet.conf

\#关闭所有carpet指令,可以在后面启用你需要的特性,玩家进入游戏后,看不到任何carpet指令和特性,除非你在下面开启 

locked

\#例如下面的特性开启 

scriptsAutoload true 

renewableCoral true



本文为我原创

[ Minecraft ](https://search.bilibili.com/article?keyword=Minecraft&from_source=article)[carpet ](https://search.bilibili.com/article?keyword=carpet&from_source=article)[地毯端](https://search.bilibili.com/article?keyword=地毯端&from_source=article)