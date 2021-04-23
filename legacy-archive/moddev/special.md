---
title: 参数帮助与模板额外内容
autoGroup-3: 进阶内容
---

# 参数帮助与模板额外内容

## label showpoem

```renpy
    call showpoem(poem=None, music=True, track=None, revert_music=True, img=None, where=i11, paper=None, chinese=True)
```

### poem
**必须配置的参数。** 指定需要显示的诗，需要在 `game\advanced_scripts\poems.rpy` 中定义内容。

### music
指定是否更改 BGM。默认为 `True`。

### track
强行指定展示诗词时的背景音乐，需指定具体文件位置。（？）

默认为 `None`。

### revert_music
指定是否在结束阅读诗词时切换回原版的 Okay, Everyone!

默认为 `True`。

### img
指定结束展示诗词时展示的立绘，如 `img="yuri eyes"`。

默认为 `None`。

### where
指定立绘展示的位置，默认为 `i11`。

### paper
指定使用某张图片来修改稿纸背景。默认为 `None`。

### chinese
<a-tag color="pink">中文模板特殊参数</a-tag>

指定是否使用中文字体展示诗歌，默认为 `True`。

如果使用 `True`，则默认使用中文字体。如果为 `False` 则使用原游戏的英文字体，但同时将无法展示中文字符。

## image bg club_day_skill

<a-tag color="pink">中文模板特殊参数</a-tag> <a-tag color="orange">内容警告</a-tag>

```renpy
    scene bg club_day_skill
```

::: warning 警告
使用本背景前请务必注意增加内容警告，且照顾 Sayori 厨的感受（（（
:::

强制使用带 Sayori 【数据删除】海报的部室背景图。（在预览图内展示为 `ignore this`）

图片预览：

![](https://cdn.jsdelivr.net/gh/DokiMod/dokimodcn-assets@master/bg_club-skill.png)

## image yuri eyesfull

<a-tag color="pink">中文模板特殊参数</a-tag> <a-tag color="orange">内容警告</a-tag>

```renpy
    show yuri eyesfull at t11
```

直接显示 Yuri 三次元之眼贴图。

## image natsuki glitch1_noanimation

<a-tag color="pink">中文模板特殊参数</a-tag> <a-tag color="orange">内容警告</a-tag>

反色的 Natsuki `4e` 你喜欢吗（（（