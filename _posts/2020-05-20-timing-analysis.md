---
layout: mypost
title: 【WIP】Cytoid & Cy2Unity 写谱 Timing 教程
categories: [写谱]
---

这篇文章将会简单介绍一些音游写谱时处理乐曲 Timimg 的方法，包括 BPM & Offset 测量和时间轴校准等，需要一定（入门级别）的乐理知识，虽然标题是 Cytoid，但是所述的方法适用于大部分音游。

## 0. 前置知识

### Malody

Malody 是由一群热爱音乐的人开发的多平台音游，谱面来自玩家自制，现在加入社区开始你的探索之旅吧~

内置的编辑器可以自动测量 BPM & Offset（仅限单 BPM），并且会自动转换乐曲为 OGG 格式。

### osu!

~Click The Circles~

棒到不行的 PC 端免费音乐游戏，内置的编辑器可以手动测量 BPM & Offset。

## 1. 获取 BPM & Offset 的方法

### A - 利用现成谱面

最简单的方法。在 osu! 和 Malody 社区中，Ranked 和 Stable 谱面的 BPM & Offset 一般都是比较准确的，可以直接照抄。但是照抄之后建议使用这些谱面中自带的音频文件，其中 Malody 自带的音频文件一般为 OGG，而 osu! 为 MP3。

#### 使用 osu!

首先去 [osu! 官网](https://osu.ppy.sh/) 或 [小夜 osu! 镜像站](https://osu.sayobot.cn/) 检索对应乐曲、下载谱面后导入游戏。

然后在主页点 Edit，找到您导入的谱面，打开后界面类似下图（图为 osu!mania 模式）：

![](https://cdn.jsdelivr.net/gh/fujao-time/fujao-time.github.io/res/timing/timing1.png)

点击上方 Timing 菜单，选择 Timimg Setup Panel，在弹出窗口右上方选择 Timing Points，页面类似下图：

![](https://cdn.jsdelivr.net/gh/fujao-time/fujao-time.github.io/res/timing/timing2.png)

然后即可在右侧列表中选择每个 Timing 节点后在左侧查看对应的 BPM & Offset 以及拍子信息了。

#### 使用 Malody

首先去 Malody 游戏内下载谱面，然后在选曲界面中选择乐曲，点击左上角 Edit 后找到编辑谱面，页面类似下图（图为 Key 模式，4.3.7 版本）：

![](https://cdn.jsdelivr.net/gh/fujao-time/fujao-time.github.io/res/timing/timing3.png)

点击右侧工具条处从上往下数第 5 个菜单，然后在子菜单选择 Information，往下滑动就可以看到第一段的 BPM & Offset（偏移），页面类似下图：

![](https://cdn.jsdelivr.net/gh/fujao-time/fujao-time.github.io/res/timing/timing4.png)

在这页底下有个【自动测量】的按键，稍后本教程会讲解其用法。

返回到主菜单后点击点击右侧工具条处从上往下数第 2 个菜单即可看到每一段的 BPM，左边一列为开始变速的拍数，右边为该段的 BPM，页面类似下图：

![](https://cdn.jsdelivr.net/gh/fujao-time/fujao-time.github.io/res/timing/timing5.png)

### B - 使用 Malody 自动测量

这也是比较方便快捷的一种方法。不管社区中有无该乐曲的谱面，只要您下载到了乐曲的 MP3 音频文件，都可以在 Malody 中使用上文所述的【自动测量】功能直接得到乐曲的 BPM & Offset 并得到 OGG 格式的乐曲副本。

首先打开 Malody，进入选曲页面，将您准备好的乐曲 MP3 拖入 Malody 中，会转换格式。

![](https://cdn.jsdelivr.net/gh/fujao-time/fujao-time.github.io/res/timing/timing6.png)

接下来，游戏会提问是否用该乐曲创作谱面，选择【是】，玩法类型选择 Key 即可，会进入编辑界面。

![](https://cdn.jsdelivr.net/gh/fujao-time/fujao-time.github.io/res/timing/timing7.png)

此时编辑器会提问是否自动测定 BPM & Offset，当然选择【确认】了，稍等片刻后编辑器会显示测定结果。

![](https://cdn.jsdelivr.net/gh/fujao-time/fujao-time.github.io/res/timing/timing8.png)

此时除了读数之外，还需要注意【不稳定度】项目，一般情况该项为 0 则说明乐曲不包含变速。如果其数值过大，表明该乐曲可能包含变速的部分。此时编辑器自动测定的结果可能不稳定，需要使用手动测量。

测量完成后，请退出游戏，进入 Malody 的安装目录，双击打开 `beatmap` 文件夹，寻找以 `_temp_` 开头的文件夹，在里面找到编辑器输出的 OGG 格式的乐曲，其文件名一般为一串数字。

### C - 使用 osu! 手动测量

最后的方案，相对比较麻烦，一般是变速乐曲没法自动测量的时候才会用。~~反正我没写过 Timing 这么复杂的变速曲，也没用过这种方法~~

不过这个方法动作要领很简单，只需要跟着节拍点就可以了！！1111

### 2. 校准时间轴 For Cy2Unity

【在做了！！1111】