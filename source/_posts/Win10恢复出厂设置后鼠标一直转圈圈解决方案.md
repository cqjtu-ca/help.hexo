---
title: Win10恢复出厂设置后鼠标一直转圈圈解决方案
date: 2019-08-31 11:11:12
tags: 系统问题
---
Windows 10恢复出厂设置后鼠标点右键一直转圈圈，很久才有反应。
本文作者：网络
本文编辑：梅健 林志杨
<!--more-->
<hr>

1. 按下键盘组合键“**Win+R**”（即同时按下键盘上的“**视窗键**”和字母“**R**”键）启动**运行**，输入“**regedit**”，点击**确定**。

![](./1.png)

2. 进入注册表编辑器，然后点开“**HKEY_CLASSES_ROOT**”，找到“**HKEY_CLASSES_ROOT\Directory**”

![](./2.png)

3. 双击展开文件夹，直到找到“**HKEY_CLASSES_ROOT\Directory\BackgroundShellex\ContextMenuHandlers**”。最后删除**ContextMenuHandlers**中除了**new**以外的文件夹。

![](./3.png)

4. 有可能除了**new**还会有一个文件夹删除不了，不过没关系，试试右键桌面看看速度如何，还不行的话重启后就行了。

<hr>

[文章纠错](https://github.com/cqjtu-acm/help/issues) | 看不懂 | 投稿 | 提建议：477897024 (QQ群)

