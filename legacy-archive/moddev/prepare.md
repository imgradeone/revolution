---
title: 准备工作
autoPrev: fontdl
---

# 准备工作

::: warning 提示
本页面仍在施工，故内容不完整。
:::

开始 Mod 开发前，需要做一些准备。

## Ren'Py SDK 6.99.12.4

DDLC 使用 Ren'Py 这款 awesome 的视觉小说引擎进行开发，因此制作 Mod 也就自然需要它了。

为避免 SDK 跨版本导致 Mod 兼容性问题，同时由于 DDLC 的 Ren'Py SDK 使用的就是 6.99.12.4 版本，请务必下载 Ren'Py SDK 6.99.12.4 进行 Mod 开发。

> 由于模板原因，中文模板暂不支持使用 Ren'Py SDK 7 进行开发，您可能需要考虑使用[这款改进过的英文模板](https://github.com/GanstaKingofSA/DDLCModTemplate2.0)，并自行配置，使字体支持中文。

**您可以点击 [这里](https://www.renpy.org/release/6.99.12) 前往 Ren'Py 官网并获取 Ren'Py SDK 6.99.12.4。**

选择版本时 **直接点击绿色的按钮** 即可。

> 一定要细说的话，Windows 系统下载 `.7z.exe` 版本，macOS 则为 `.dmg`，Linux 为 `.tar.bz2`。 **不确定的话可以直接下载 `.zip` 版本。**  
> 顺便，Android 和 iOS 等手机端用户就别凑热闹了，Mod 的调试只能使用电脑（当然可以拿手机先写代码）（（（

## DDLC 游戏文件

既然是 DDLC Mod，肯定需要 DDLC 的文件才可以进行调试。 ~~不然写个锤子的 Mod~~

前往 [DDLC.moe](https://ddlc.moe) 或者 [Steam](https://store.steampowered.com/app/698780/) 下载 DDLC 游戏本体，解压，**不要打开游戏**，先备用。

## 中文字体包

> 如果你使用英文模板，可以忽略这一步。

中文字体包的下载请查看 [这里](./fontdl)。

## 中文 Mod 模板 / 你想要的 Mod 模板

既然这里是中文 Mod 模板的官网，考虑下用用中文 Mod 模板呗（（（

我们这里提供了 3 种 DDLC Mod 模板，但只有中文模板预先配置好了中文开发相关内容。其它模板如需要使用中文，请自行配置。

接下来的教程以中文模板为主。

[中文模板](https://github.com/imgradeone/DDLCModTemplete-Chinese/releases) | [原版英文模板](https://github.com/Monika-After-Story/DDLCModTemplate) | [改良版英文模板](https://github.com/GanstaKingofSA/DDLCModTemplate2.0)

将模板文件解压到刚刚你解压 Ren'Py SDK 的文件夹里，或者在你指定的工程目录里。（默认情况下，是 `renpy-6.99.12.4-sdk`）

接下来，打开你存放原版 DDLC 游戏的文件夹，将游戏目录下 `game` 文件夹内的 `audio.rpa`、`images.rpa` 和 `fonts.rpa` 复制到工程文件夹（即你解压模板文件的地方）。（千万不要把 `scripts.rpa` 一并复制过去，会出现冲突）

将下载的中文字体包解压到工程的 `/game/mod_assets/font/` 文件夹下。

最后，在 Ren'Py SDK 里启动工程，如果正常运行，恭喜，你现在可以准备开发 Mod 了！

## 合适的文本 / 代码编辑器

只有使用合适的编辑器，才能让你的写代码体验更加舒适。这个“合适”其实是一个很主观的概念，**只要你觉得合适，那它就是合适。** ~~（所以就算你用 Windows 自带的记事本去写 Ren'Py 脚本，我也不拦你（（（）~~

我个人使用的是 [Visual Studio Code](https://code.visualstudio.com)，是微软出的一款很 awesome 的编辑器，在 Marketplace 安装了 [Ren'Py 高亮插件](https://marketplace.visualstudio.com/items?itemName=LuqueDaniel.languague-renpy)后，写 Ren'Py 脚本特别舒服。  
如果你不希望微软用什么 Telemetry 来收集你的隐私，或者你抵制微软却又很想用 VS Code，你也可以试试 [VSCodium](https://vscodium.com)，是去除了微软要素的 VS Code，尊重隐私且更尊重开源社区。~~（GNU 教徒可以试试？）~~

当然，还有其他文本 / 代码编辑器，比如 [Atom](https://atom.io/)、[Sublime Text（需付费，但可长期评估）](https://www.sublimetext.com)，你都可以选用，或者不必迁移，直接使用你最喜欢的编辑器去写 Mod。

顺便，Atom 其实是 Ren'Py 7 官方推荐的编辑器，原生支持 Ren'Py 脚本高亮。

~~（其实你拿 Vim / Emacs 写，我都没意见，只是很麻烦（（（~~

~~（你拿写 Vue 的 HBuilder X 写，我其实也没意见，但是这不太好吧（（（~~

::: warning 警告！！！
请不要使用 Editra 进行 Mod 编写，因为此编辑器完全不支持中文输入，甚至有可能破坏你的工程（？）。
:::

## 合适的 Git GUI

> 命令行大佬请直接忽略这一节  
> （前提是你可能有意开源你的 Mod，无意的话你也可以使用 Private 仓库）
> 当然你可以用编辑器自带的 Git 管理，VS Code 的工作区功能其实也很好用

### GitKraken（半付费）

GitKraken 虽然并不是我常用的 Git GUI，但是它非常爽。标签系统让你更快切换多个 Repo，一个视角尽览各个 commit，功能很齐全，甚至内置了编辑器（虽然这个功能某些情况下要付费）。

对于 GitHub 个人 / 团队，且**不使用私有仓库（Private Repo）**的用户来说，这个客户端完全够用，且**基本上免费**，不用担心太多问题。

支持 Windows、macOS、Linux，且支持 32 位 Windows 系统。

~~当然给好朋友看你那一排花里胡哨的 commit 列表也挺 awesome 的~~

[官网](https://www.gitkraken.com)

### GitHub Desktop

GitHub Desktop 是一款简洁的 Git GUI，如果你使用 GitHub，且不太熟悉 Git，可以试一下。它包含了你所需要的 Git 功能，也对 GitHub 有更好的支持，简单易懂，几个傻瓜式操作就完事。

支持 Windows 和 macOS，不支持 Linux。

[官网](https://desktop.github.com) （但不保证下载得了 XD）

### Sublime Merge（付费，但可长期试用）

Sublime Merge 是一款来自 Sublime Text 开发者的 Git GUI，侧重于提供 Git 命令行的原始体验（借助命令面板）。UI 十分简洁、易用，有种 macOS 的即视感，也有类似 GitKraken 的 commit 关系图。

支持 Windows、macOS、Linux。

[官网](https://www.sublimemerge.com)

----------

准备完这些后，就可以开始你的 Mod 编写与开发了。

## 最后的准备

将模板文件夹重命名为你想要的工程名（建议英文），接下来打开 Ren'Py SDK。

下文的开发将假设你使用简体中文版 Ren'Py SDK 界面，所以，点击 `preferences`，将 Language 更改为 `Simplified Chinese`。

接下来，翻到下一篇文章，开始 Mod 开发吧！