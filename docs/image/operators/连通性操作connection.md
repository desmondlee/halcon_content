---
weight: 3
date: 2020-12-27
title: "连通性操作connection"
---

# 连通性操作connection

### 作用

将整体目标拆分成多个独立目标。

### 前提

需要通过`threshold`标注出目标。

## 使用方式

命令`connection (Regions, ConnectedRegions)`。

其中，第一个参数 `Regions`是通过`threshold`得到的变量，第二个变量`ConnectedRegions`是connection算子的输出变量。

执行该命令后，包含在整张图像中的多个目标就被拆分成多个独立目标。(如果右键单击图像，彩色数量选择12，会发现每个独立的目标都被着上了不同的颜色)

### 参考图

![连通性操作](http://qn.halcon.lizhenguo.cn/image/connection1.png)