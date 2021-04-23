---
title: 第一个 Label
autoPrev: prepare
---

::: warning 提示
本页面仍在施工，故内容不完整。
:::

# 第一个 Label

现在，打开你的文本编辑器，并且在编辑器中打开你的工程文件夹。

接下来，打开 `/game` 文件夹下的 `script.rpy`，这里存放着游戏的基本运行逻辑。

你应该会看到这样一个文件：

```renpy
# /game/script.rpy

label start:

    $ anticheat = persistent.anticheat # 可以忽略

    $ chapter = 0 # 目前可以忽略

    $ _dismiss_pause = config.developer # 可以忽略

    # 可以修改女主的名字
    $ s_name = "Sayori" # 可选译名：纱世里（推荐）、莎世里、纱悠里
    $ m_name = "Monika" # 推荐译名：莫妮卡
    $ n_name = "Natsuki" # 可选译名：夏树（推荐）、娜苏琪
    $ y_name = "Yuri" # 推荐译名：优里

    $ quick_menu = True
    $ style.say_dialogue = style.normal
    $ in_sayori_kill = None
    $ allow_skipping = True
    $ config.allow_skipping = True
    
    # 确定好 label，然后改动下面几行
    if persistent.example_seen:
        call tutorial_selection from _call_tutorial_selection
    else:
        call example_chapter from _call_example_chapter
    # 就动注释夹起来的这几行

    # 对于教程，直接使用下面一行：
    # call meet_monika

    return

label endgame(pause_length=4.0):
    $ quick_menu = False
    stop music fadeout 2.0
    scene black
    show end
    with dissolve_scene_full
    pause pause_length
    $ quick_menu = True
    return
    # 可以忽略
```

其中，有几行你大可忽略，我在这个文档里也标记了一下。

顺便解释一下，Ren'Py 的 label 指明了某一个脚本，而 `start` 这个 label 实际上很特殊，它指定了你点击 `新游戏` 按钮后会执行的脚本。

下面的 `endgame` label 则是某周目结束后显示显示 `END` 的脚本，你可以先忽略。

而你真正需要修改的，是脚本的第 22 行。（1.2 模板正式版则为 26 行）

```renpy
# /game/script.rpy - line 22-30

    # 确定好 label，然后改动下面几行
    if persistent.example_seen:
        call tutorial_selection from _call_tutorial_selection
    else:
        call example_chapter from _call_example_chapter
    # 就动注释夹起来的这几行

    # 对于教程，直接使用下面一行：
    # call meet_monika

```

将这几行直接修改为以下内容，注意开头的 4 个空格缩进：

```renpy
    call meet_monika
```

（当然你不需要按 4 下空格键，一些编辑器可以用 Tab 键补全这四个空格缩进）

下一步新建一个文件，命名为 `meet_monika.rpy`，记得扩展名。

然后输入以下内容：

```renpy
# /game/meet_monika.rpy
label meet_monika:
    
    mc "DDLC 太好玩了！"
    y "就是啊，Monika 多可爱啊！"
   
    return
```

运行一下工程，点击 `新游戏`，你应该可以看到你和 Yuri 的一段对话，只是 BGM 和背景都出现了一些问题，不像是个正经 Mod。

不过，你的写 Mod 之路从此正式开始了！

接下来，我们会让这个脚本更加丰富，跟着教程继续完成吧！