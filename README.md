<!-- omit in toc -->
# Rime·徐码·尔雅输入法

forFudan

```txt
更新：
- 2022年3月31日 初版
- 2023年3月7日 本方案现在提供CJK所有汉字或部首的全字拆分，共计98446个字符，提供基于《古籍印刷通用字规范字形表》的繁体方案。
- 2023年5月5日 基于宇浩输入法的拆分，添加对于 CJK-I 区603个汉字的支持以及全字拆分提示。
```

- [1. 介绍](#1-介绍)
  - [1.1. 徐码·尔雅输入法·2023年新版](#11-徐码尔雅输入法2023年新版)
  - [1.2. 徐码教程](#12-徐码教程)
  - [1.3. 本方案](#13-本方案)
- [2. 使用](#2-使用)
  - [2.1. Windows / Macos / 安卓安装方法](#21-windows--macos--安卓安装方法)
  - [2.2. 具体文件介绍](#22-具体文件介绍)
- [3. 方案特点](#3-方案特点)
  - [3.1. 提示快捷键](#31-提示快捷键)
  - [3.2. 单字拆分三重注解](#32-单字拆分三重注解)
  - [3.3. 单字简码调整](#33-单字简码调整)
  - [3.4. 二级简码矩阵](#34-二级简码矩阵)
  - [3.5. 词语简码调整](#35-词语简码调整)
  - [3.6. 标点符号二简快速输入](#36-标点符号二简快速输入)
  - [3.7. 增广常用字符集](#37-增广常用字符集)
  - [3.8. 一键切换字符集](#38-一键切换字符集)
  - [3.9. 使用 \` 键引导四叶草拼音输入和反查](#39-使用--键引导四叶草拼音输入和反查)
  - [3.10. 全码词语屏蔽](#310-全码词语屏蔽)

## 1. 介绍

### 1.1. 徐码·尔雅输入法·2023年新版

徐码·尔雅输入法是由徐国银先生发明的一种优秀的形码输入法方案，特点为双编码。优点包括：繁简通打、支持CJK大字集、低重码、全码简码一致、字词编码一致等。官方网站：<http://xumax.cn/> 官方QQ群: 761401688

这里对比一下五笔、郑码、徐码、虎码在不同汉字字符集下的单字全码的重码数量，以供参考。这些都是我比较喜欢、有亮点的输入法。仓颉虽然是五码定长，但它在繁体输入上地位很高，所以也将它纳入比较。加粗的数字代表本行最优值。排名按发明时间顺序：

| 形碼方案 |  簡體GB2312 | 國字常用 | 常用繁簡 |      GBK | 簡體選重率 | 繁體選重率 | 繁簡選重率 |
| :------- | ------: | -------: | -------: | -------: | ---------: | ---------: | ---------: |
| 鄭碼     |     563 |      311 |     1784 |     6590 |      0.60% |      0.63% |      2.40% |
| 五筆86   |     537 |      357 |     1718 |     6582 |      0.34% |      0.79% |      2.12% |
| 五筆98   |     515 |      329 |     1656 |     6368 |      0.38% |      0.78% |      2.16% |
| 徐碼23   |     **318** |  **127** |  **480** |     2902 |      0.11% |      0.22% |      0.22% |
| 倉頡五代 |     422 |      164 |      606 | **2893** |      0.89% |      0.49% |      1.06% |
| [宇浩](https://zhuyuhao.com/yuhao)     | 320 |      216 |      606 |     4971 |  **0.05%** |  **0.16%** |  **0.18%** |

这里列出各维度上同其它四码定长输入法之间比较，排名越靠前越好：

| 维度                           | 第一                | 第二 | 第三        | 第四   | 第五   | 第六   |
| ------------------------------ | ------------------- | ---- | ----------- | ------ | ------ | ------ |
| 简体静态重码重码数量           | 宇浩 ~ 徐码         |      | 五笔98      | 虎码   | 五笔86 | 郑码   |
| 简体动态重码率                 | 虎码 ~ 宇浩         |      | 徐码        | 虎码   | 五笔86 | 五笔98 | 郑码 |
| 对繁体字输入进行特别优化             | 宇浩 ~ 徐码         |      | 郑码        | 五笔98 | 五笔86 | 虎码   |
| 常用字简繁通打静态重码重码数量 | 徐码                | 宇浩 | 虎码        | 郑码   | 五笔98 | 五笔86 |
| 常用字简繁通打动态重码率       | 宇浩 ~ 徐码         |      | 五笔86      | 五笔98 | 郑码   | 虎码   |
| 大字集重码数量                 | 徐码                | 宇浩 | 五笔98      | 五笔86 | 郑码   | 虎码   |
| 字根设置整体性                 | 郑码                | 徐码 | 宇浩        | 虎码   | 五笔   |        |
| 键盘区位聚合度                 | 五笔                |      | 宇浩        | 郑码   | 徐码   | 虎码   |
| 编码规则简易度                 | 虎码                | 宇浩 | 郑码 ~ 五笔 |        |        | 徐码   |
| 全简一致（简码、词语编码）     | 五笔=徐码=虎码=宇浩 |      |             |        |        | 郑码   |
| Z 键使用                       | 五笔=宇浩           |      |             | 虎码   | 郑码   | 徐码   |

由上表可见，徐码在各个字集的重码表现都非常亮眼。

### 1.2. 徐码教程

[點擊此處閱讀我所寫的《徐碼輸入法簡明教程》（繁體版）來瞭解和學習徐碼。](tutorial.md)

[![徐碼字根圖](/resources/徐碼全字根圖.png)](/resources/徐碼全字根圖.png)

### 1.3. 本方案

本方案在2023年1月15日官方码表基础上进行深度定制。挂载于RIME平台（小狼毫、鼠须管）<https://rime.im/>。其具有以下特点：

- 提供至 CJK-I 区、兼容区、部首区超过99000个汉字的完整拆分、编码提示、字集提示。
- 为简化字和繁体字重新设置一级简码和二级简码。
- 支持二级简码快速标点符号输入。
- 支持自定义字符集过滤生僻字。常用字约一万字，包括 GB2312 汉字、國語常用字、其它常用汉字等。支持用户自定义修改。
- 提供四码只出单字功能，适合单字派。

## 2. 使用

### 2.1. Windows / Macos / 安卓安装方法

在安装了 Rime（小狼毫、鼠须管、同文）后，将 [/schema](https://github.com/forFudan/xuma/tree/main/schema) 文件夹下的所有文件复制到 Rime 目录下。同时在 default.custom.yaml 文件中加入以下内容：

```yaml
patch:
  schema_list:
    - schema: xuma_forfudan
```

点击「部署」之后即可使用。

### 2.2. 具体文件介绍

文件介绍：

- xuma_forfudan.schema.yaml 简体方案文件
- xuma_forfudan.dict.yaml 简体字典文件
- xuma_forfudan.words.dict.yaml 拓展词库
- rime.lua 脚本设定
- lua/forfudan_freq_filter.lua 字符集过滤脚本。可添加自定字符。
- opencc/... 單字拆分表
- build/clover... 已编译好的四叶草拼音文件。或者自行安装。<https://github.com/fkxxyz/rime-cloverpinyin>

## 3. 方案特点

### 3.1. 提示快捷键

输入`help`可显示快捷键提示。

### 3.2. 单字拆分三重注解

提供至CJK-H区、兼容区、部首区超过98000个汉字的完整拆分、编码提示、字集提示。拆分提示中包括三重注解：

1. 该汉字的完整拆分（所有部件）。
2. 该汉字的全码。使用大小写字母区分大小码，便于初学者分辨主、副根字。
3. 该汉字所在的字符集（GB2312，GBK，CJK，CJK A 到 H 区，兼容字等）。

用户还可通过「Shift+Ctrl+C」切换拆分状态。

### 3.3. 单字简码调整

本方案根据简化字体系下的字频数据，调整了一级、二级、三级单字简码。其中，一级简码调整如下（共8个）：

- A「以」改为「能」。否则「能」字需要`asv`三码出字。
- C「发」改为「好」。因为「好」字频更高。且让出了二简位给同样高频的「她」字。
- D「那」改为「对」。否则高频「对」字需要`dico`四码出字。
- H「在」改为「有」。否则高频「有」字需要`hsv`三码出字。
- M「同」改为「见」。否则高频「见」字需要`mve`三码出字。
- N「国」改为「当」。否则高频「当」字需要`nbu`三码出字。
- S「得」改为「然」。
- Z「为」改为「没」。否则「没」字需要三码出字，且`zqs`会在左手小指，非常不便。

二级简码也作部分调整，比如：

- xq 码位由「将」改为「次」，否则需要`xqqs`四码出字。

特别的，部分字频不高的繁体字和传承字字根移到三选。这样可以腾出一个二简码位用于高频字。例如：

- 「艮0.00%」移到三选，同时将码位让给「司0.05%」
- 「巳0.00%」移到三选，同时将码位让给「通0.06%」
- 「殳0.00%」移到三选，同时将码位让给「解0.07%」
- 「冊0.00%」移到三选，同时将码位让给「内0.08%」
- 「韋0.00%」移到三选，同时将码位让给「尽0.04%」
- 「戊0.00%」移到三选，同时将码位让给「太0.10%」
- 「缶0.00%」移到三选，同时将码位让给「年0.18%」
- 「歹0.00%」移到三选，同时将码位让给「五0.06%」
- 「臣0.01%」移到三选，同时将码位让给「打0.15%」
- 「瓜0.01%」移到三选，同时将码位让给「后0.34%」
- 「虫0.01%」移到三选，同时将码位让给「些0.20%」
- 「申0.00%」移到三选，同时将码位让给「明0.15%」
- 「烏0.01%」移到三选，同时将码位让给「今0.07%」
- 「馬0.09%」移到三选，同时将码位让给「现0.22%」
- 「弋0.00%」移到三选，同时将码位让给「式0.03%」
- 「匕0.00%」移到三选，同时将码位让给「条0.05%」
- 「舟0.00%」移到三选，同时将码位让给「种0.14%」
- 「髟0.00%」移到三选，同时将码位让给「妻0.01%」

同时，我们为所有字根增加**替身码**，重复其小码即可实现输入。例如：

- 艮 `bgg`
- 巳 `dss`
- 殳 `qss`

### 3.4. 二级简码矩阵

[点击此处，查看二级简码矩阵。](second_level_matrix.md)

### 3.5. 词语简码调整

本方案根据简化字体系下的词频，调整了一级、二级词语简码。

值得注意的是，在官方码表中，二简二选词语取两个字首码。这导致词语全码简码不一致。在本方案中，统一调整取消这种取码方式。

关于简码词的设置有一些原则：

- 词频越靠前，设置简词的可能性越高。
- 如果简词的第一个字在二简一选位，则优先放在二简。例：「毕竟」，因为「毕」是二简字，所以「毕竟」也设成二简而不是一简。
- 接上，如果简词的频率过高，仍然设在一简。例：「如果」，虽然「如」是二简字，但是「如果」的词频太高，所以放在了一简位上。

一简码位都有二选简词和三选简词。

二简码位不一定有两个简词。如果一个词没有重码，那么将它设在二简位只省了一个按键，还会增加记忆负担，故而二简词只在以下情况下会设置：

1. 一个词的词频非常高，故而提供简码位。
2. 一个词的全码输入时不符合人体工学。

### 3.6. 标点符号二简快速输入

对于一些使用频率不高的二简码位，提供标点符号的快速输入，包括：

- 「」，单方引号，aj
- 『』，双方引号，ak
- “”，双圆引号，ah
- ‘’，单圆引号，ai
- 〔〕，六角引号，al
- ：，冒号，mm
- 《》，书名号，sm
- ！，感叹号，gg
- ？，问号，ww
- ——，破折号，pp
- ……，省略号，sl
- ×，隐讳符，yh
- □，缺字符，qz
- 々，叠字符，dz，也可以通过 qwu 输入。
- ·，间隔符，yy
- §，章节号，zj
- 、，顿号，nn
- ，，逗号，oo
- 。，句号，jj
- 全角空格，dl

### 3.7. 增广常用字符集

本方案使用了自定的常用字符，将常用字一网打尽，避免了 RIME 内置字符集「GB2312字太少，GBK字太多」的问题。包括了以下一万个左右的字符：

- GB2312 全部字符
- 台湾的「国字常用字」
- 注音符号
- 「〇」符号
- 「镕」等 GB2312 未收录的常用简化字
- 「喆裏墻粧嫺綫綉滙峯」等「国语常用字」未收录的常用繁体字
- 「咲雫乭」等常见日韩汉字

### 3.8. 一键切换字符集

在输入过程中，用户可选择两种切换字集的方式：

- 通过「Shift+Ctrl+O」在常用字符集和CJK大字符集之间进行切换（过滤）。
- 通过「Shift+Ctrl+I」将常用字符集优先显示（优先）。

用户还可通过「Shift+Ctrl+F」进行简入繁出输入。

### 3.9. 使用 ` 键引导四叶草拼音输入和反查

按下 ` 键，可以随时使用四叶草拼音输入词语，并实现反查。四叶草拼音：<https://github.com/fkxxyz/rime-cloverpinyin>

### 3.10. 全码词语屏蔽

一键屏蔽四码词语，同时保留简码词。热键为「Shift+Ctrl+D」。适合保留简码词的全码单字派。
