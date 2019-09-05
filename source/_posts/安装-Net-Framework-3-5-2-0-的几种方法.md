---
title: 安装.NET Framework 3.5(2.0)的几种方法
date: 2019-08-03 20:53:11
tags: 软件安装
---
安装.NET Framework 3.5(2.0)的几种方法。
本文作者：林志杨
<!-- more -->
<hr>

> ## 方法一：使用 “启用Windows功能” 安装

### 详细步骤：

1. ***点击*** 任务栏左下角中的 **“放大镜”按钮** *（图中红色箭头所指的红色框框里）* 或者 **“圆圈”按钮** *（图中蓝色箭头所指的蓝色框框里）* ，然后使用输入法直接 ***输入*** **“Windows功能”**，如图所示，***选择*** **“启用或关闭Windows功能”** 

<img src="./搜索_Windows功能.png" width="40%" />


> * 上文中的 **“放大镜”按钮** 在 **Windows 1903及以上** 的版本才有，
如果你的电脑上没有，点击 **“圆圈”按钮** 效果是一样的。

> * *使用输入法直接输入* 的意思是使用键盘打出英文字母和汉字。


2. 如图所示，***选中*** **.NET Framework 3.5(包括 .NET 2.0 和 3.0)**

![](./设置_Windows功能.png)

3. ***点击*** **确定** 按钮，会自动开始安装

---

> ## 方法二：使用 DISM程序 安装

**DISM** 是Windows系统自带的一个程序，可以使用它来安装 *.NET Framework 3.5* 。使用DISM.exe安装 *.NET Framework 3.5* 需要准备一个文件：*microsoft-windows-netfx3-ondemand-package.cab* 。这个文件存在于Windows的安装镜像中 *( \sources\sxs\ )*。考虑到学校的网络条件，我们从系统镜像中提取了这个文件，省去下载一个完整系统镜像的时间。

### 详细步骤：

1. ***右键*** **"开始菜单" 按钮**，然后 ***点击*** **“Windows PowerShell(管理员)(A)”** 打开PowerShell程序

<img src="./打开_Powershell.png" width="40%" />

2. ***下载*** **microsoft-windows-netfx3-ondemand-package.cab** 文件（[下载地址 1](http://files.cqjtujx.club/microsoft-windows-netfx3-ondemand-package.cab) | [网盘下载](http://pan-yz.chaoxing.com/share/info/ba6356b3e7895cfe) 密码 : **740uqc**）,并把该文件 ***移动*** 到 **C盘根目录下** 


<img src="./移动到C盘_Powershell.png" width="40%" />

3. ***输入*** 以下命令，然后 ***按下*** **回车**（即键盘上的 **Enter** 键 ）

```
    Dism.exe /online /enable-feature /featurename:NetFX3 /source:C:\ /LimitAccess
```

4. 如图，**提示“操作成功完成”**，说明安装**已经完成**。***重新启动系统*** 即可。

<img src="./输入命令2_Powershell.png" width="60%" />
<br>

<hr>

[文章纠错](https://github.com/cqjtu-acm/article/issues) | 看不懂 | 投稿 | 提建议：477897024 (QQ群)

