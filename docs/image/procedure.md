---
title: "流程"
weight: 2
date: 2020-12-24T22:59:03+08:00
draft: true
---

# 流程

{{< mermaid>}}
graph TD

A[采集图像] --> B{有无判定, Blob/定位}
B --> |有| C[获得位置,角度信息]
B --> |无| A
C --> D[仿射变换, 求变换句柄, ROI变换]
D --> E[图像预处理]
E --> F[图像处理]
F --> G[结果输出]
{{</ mermaid>}}
