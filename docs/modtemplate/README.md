---
title: DDLC 中文 Mod 模板
article: false
permalink: /modtemplate/
date: 2021-04-25 18:05:54
---

# DDLC 中文 Mod 模板

嘿，你~~又~~想用中文写 DDLC Mod？**那你来对地方了！**

这是**全新的** DDLC 中文 Mod 模板！本模板基于 GanstaKingofSA 的 [DDLC Mod Template 2.0](https://github.com/GanstaKingofSA/DDLCModTemplate2.0)，并得到了旧版已经进行的一系列汉化。使用本模板制作 Mod 时，请遵循 Team Salvato 的 [IP Guidelines](https://revolution.dokimod.cn/ipguidelines.html)。

当前版本的模板支持 Ren'Py SDK 6.99.12 及 7.4.5。

**本模板是为使用原版 DDLC 素材的饭制游戏和 Mod（而并非不使用原版素材的作品）设计的，提供源代码也并非以便将其复制粘贴到和 DDLC 没有关系的工程。此模板内大部分代码属于 Team Salvato 的知识产物，请遵循 Team Salvato 的 [IP Guidelines](https://revolution.dokimod.cn/ipguidelines.html) 使用，否则后果自负。**

**如果你是 Mod 作者，请不要将 DDLC 游戏本体包含在你分发的 ZIP 里，这是违反 IP Guidelines 的行为。**

> 目前 Ren'Py SDK 7.4.6-7.4.7 有破坏性改动，会导致 DDLC 转场失效，请暂时不要更新 SDK！！！更多详情请参考 [此 Issue](https://github.com/renpy/renpy/issues/2860)。

> 本 Mod 模板不支持 Doki Doki Literature Club Plus。

> 请注意：本模板可能尚不完善，且尚缺乏繁体中文支持。部分 GUI 元素暂未被汉化。

> 此模板自带 Android 支持，详情请看原版 DDLC Mod Template 2.0 所附带的 `guide.pdf`，或在稍晚时候访问 [DokiMod 开发文档](https://docs.dokimod.cn) 了解 Android Mod 制作方式。

> 提示：本模板**仅在 [GitHub](https://github.com/imgradeone/DDLCModTemplate-Chinese-next/releases/)、[Gitee](https://gitee.com/imgradeone/DDLCModTemplate-Chinese-next/releases/) 和 [git.ddlc.top](https://git.ddlc.top/imgradeone/DDLCModTemplate-Chinese-next/releases) 提供下载，完全免费**。你可能在 CSDN 看到了这个模板，**不要去那边花冤枉钱下载**！！！（目前已知的 CSDN 盗传版是 1.x 版本，已经不受维护。）  
> 此后本模板不再考虑托管于 SourceForge。（鉴于托管于 SourceForge 会加大恶意爬虫与盗传的概率）
> Gitee 镜像源的版本更新不及时，但可作为中国大陆加速源。

您可以查看 [更新日志](CHANGELOG.md)。

## 开始制作 Mod

::: cardList 2
```yaml
- name: 查看开发文档，请前往 DokiMod 开发文档站
  desc: https://docs.dokimod.cn/modtemplate/
  link: https://docs.dokimod.cn/modtemplate/
  bgColor: '#fa4694' # 背景色，可选，默认var(--bodyBg)。颜色值有#号时请添加引号
  textColor: '#ffffff' # 文本色，可选，默认var(--textColor)
```
:::

---

## 模板特色功能

### DDLC Mod Template 2.0
1. 同时支持 Ren'Py SDK 6 和 7 的 Mod 构建
1. DDLC 的原版 RPY 文件，内含注释
1. 高度可定制！这个模板只是起点，借助你的创意，做你想做
1. macOS `.app` 及 Linux `.sh` 启动文件制作支持
1. 完整的 Android 支持！DDLC 的一切（除了 `[currentuser]` 变量）可在 Android 平台正常运行。
    > 请前往 [原版 DDLC Mod Template 2.0](https://github.com/GanstaKingofSA/DDLCModTemplate2.0/blob/master/guide.pdf) 所附带的 `guide.pdf` 了解 Android Mod 移植 / 开发。
1. Xcode 支持！您可以在 Xcode 中直接编辑、构建、测试您的 DDLC Mod，无需打开 Ren'Py 启动器。
    > 提示：您需要更改 `RENPY_TOOL` 变量，将其定位到您的 Ren'Py SDK 应用程序位置。[了解更多 &rsaquo;](XCODE.md)
1. Terra 的深度诗词游戏教程（WIP）
1. NVL 模式支持 - 特别感谢 Yagamirai01
1. [BETA] 人称支持！现在用户可以自行选择符合自己的人称了！
    > This works best with `He/Him`, `She/Her`, and `They/Them` pronouns but this can be expanded on as much as you like. Make sure to call `finishPronouns()` in your script after a pronoun is selected! See *pronoun_example.rpy* for a example on how to use this feature.

### DDLC 中文 Mod 模板
1. 绝赞中文化（目前只支持简体中文）
2. 绝赞字体优化
3. ~~绝赞咕咕咕~~
4. 内置汉化剧本（贡献者详见特别感谢）

## 特别感谢

- Team Salvato http://teamsalvato.com / https://ddlc.moe
- [GanstaKingofSA](https://github.com/GanstaKingofSA)
- 所有字体作者
- 社区汉化补丁团队（同时也是 DDLC Plus 饭制翻译支持者）：[DB (aka dumb)](https://steamcommunity.com/id/HomuLilly/)、[Javelin&Tea (aka J&Tea)](https://steamcommunity.com/profiles/76561198037532534/)、[TBGN](https://steamcommunity.com/id/PhyYuan/)、[Pizza Hime (aka 擎天披利)](https://steamcommunity.com/id/qweion/)
- [Riotloc 团队](https://www.riotloc.com)（DDLC Plus 官方翻译团队）

## 开源许可

本 Mod 模板需要使用 Ren'Py。  
Ren'Py 的许可，请参照 https://www.renpy.cn/doc/license.html （简体中文）或 https://www.renpy.org/doc/html/license.html （英文）。

本模板基于 GanstaKingofSA 的 [DDLCModTemplate2.0](https://github.com/GanstaKingofSA/DDLCModTemplate2.0)。

本模板属于粉丝作品，遵循 Team Salvato IP Guidelines。

## 加入社区

[Telegram 频道](https://t.me/DDLCModCN)  
[Odysee 频道](https://odysee.com/@DokiMod:1)
[Twitter](https://twitter.com/DokiMod)

---

Copyright © 2019-2021 GanstaKingofSA. All rights reserved. 

Modified and translated by imgradeone.

Doki Doki Literature Club, the Doki Doki Literature Club code, is the property of Team Salvato (Dan Salvato LLC). Copyright © 2017 Team Salvato. All rights reserved.