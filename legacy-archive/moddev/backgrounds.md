---
title: 背景添加
autoPrev: firstlabel
sidebarDepth: 2
---

# 背景添加

::: warning 提示
本页面仍在施工，故内容不完整。
:::

没有背景图片的 Mod，不是一个好 Mod，而 DDLC 的画师为游戏制作了这么多背景，为什么不好好利用一下呢？

接下来，将介绍如何添加一个背景图片。

## 从梦开始的地方起步

在 Mod 脚本里，请在对话之前，输入如下内容：

```renpy
    scene bg residential_day with dissolve_scene_full
```

完整内容如下：

```renpy {4}
# /game/meet_monika.rpy
label meet_monika:
    
    scene bg residential_day with dissolve_scene_full
    
    mc "DDLC 太好玩了！"
    y "就是啊，Monika 多可爱啊！"
   
    return
```

此时运行代码，你应该可以看到完整的转场效果和自家门口的背景了。

## 那么刚刚加的代码啥意思？

`scene` 是 Ren'Py 中显示背景图片的命令。

`bg residential_day` 则是所需要显示的图片。实际上这是经过定义的语句，您可以在 `game/advanced_scripts/definitions.rpy` 里查看所有定义过的背景，但这还是很复杂。文档下方会附带 [全部背景预览](#全部背景预览)，帮助你选择背景。

`with dissolve_scene_full` 是转场效果。（解释待补充）

一些对于新人来说没什么用的拓展：相较于 `show` 命令，`scene` 可以清空目前所有显示的背景、立绘，并直接显示新的背景。如果使用 `show` 命令，那么切换背景时会有许多问题，但使用 `scene` 就解决了这个问题。

## 全部背景预览

感谢背景画师 Velinquent 的爆肝。

### bg residential_day（家门口）

![](https://cdn.jsdelivr.net/gh/DokiMod/dokimodcn-assets@master/bg_residential.png)

调用方式（不带转场，下同）：

```renpy
    scene bg residential_day
```

### bg corridor（走廊）

![](https://cdn.jsdelivr.net/gh/DokiMod/dokimodcn-assets@master/bg_corridor.png)

调用方式：

```renpy
    scene bg corridor
```

### bg club_day（文学部活动室）

![](https://cdn.jsdelivr.net/gh/DokiMod/dokimodcn-assets@master/bg_club.png)

调用方式：

```renpy
    scene bg club_day
```

### bg club_day2

::: warning 警告
使用本背景前请务必注意增加内容警告，且照顾 Sayori 厨的感受（（（
:::

文学部活动室，但有 1/6 概率出现某个恶心的东西（恶心的东西见下方 club_day_skill）

调用方式：

```renpy
    scene bg club_day2
```

### bg club_day_skill（出现某个恶心的东西的文学部活动室）

::: warning 警告
使用本背景前请务必注意增加内容警告，且照顾 Sayori 厨的感受（（（
:::

文学部活动室，但会 100% 出现某个恶心的东西（中文模板赠送）

![](https://cdn.jsdelivr.net/gh/DokiMod/dokimodcn-assets@master/bg_club-skill.png)

调用方式：

```renpy
    scene bg club_day_skill
```

### bg closet（储物间）

![](https://cdn.jsdelivr.net/gh/DokiMod/dokimodcn-assets@master/bg_closet.png)

调用方式：

```renpy
    scene bg closet
```

### bg bedroom（MC 家的卧室）

![](https://cdn.jsdelivr.net/gh/DokiMod/dokimodcn-assets@master/bg_bedroom.png)

调用方式：

```renpy
    scene bg bedroom
```

### bg sayori_bedroom（Sayori 家的卧室）

![](https://cdn.jsdelivr.net/gh/DokiMod/dokimodcn-assets@master/bg_sayori_bedroom.png)

调用方式：

```renpy
    scene bg sayori_bedroom
```

### bg house（Sayori 家的门口）

![](https://cdn.jsdelivr.net/gh/DokiMod/dokimodcn-assets@master/bg_house.png)

调用方式：

```renpy
    scene bg house
```

### bg kitchen（MC 家的厨房）

![](https://cdn.jsdelivr.net/gh/DokiMod/dokimodcn-assets@master/bg_kitchen.png)

调用方式：

```renpy
    scene bg kitchen
```

## 纯色背景

### black（纯黑色）

调用方式：

```renpy
    scene black
```

### dark（暗色遮罩）

调用方式（使用 show 获得最佳效果）：

```renpy
    show dark
```

### darkred（血色遮罩）

调用方式（使用 show 获得最佳效果）：

```renpy
    show darkred
```

### white（纯白）

调用方式：

```renpy
    scene white
```

### end（END 字幕）

调用方式：

```renpy
    scene end
```

## 转场方式

（待补充）