---
weight: 6
date: 2020-12-27
title: "Blob"
---

# Blob

## 流程

1. 采集图像(1. 本地图像；2.相机接口)(read_image)
2. 图像分割(threshold)
3. 形态学处理(closing_circle, medium_image, erosion, dilation)
4. 连通性分析(region, connection)
5. 填充(fill_up, fill_up_shape)
6. 特征提取(直方图, 检测)(select_shape)
7. 获取结果





## 描述

- read_image

  读取图片

- threshold

  给目标物(如回形针)着色，从背景图中区分出

- closing_circle

  给threhold着色时，没有着色的部分补充着色。(根据调整参数，尽可能让需要着色的空洞能着色，不需要着色的部分不会被着色)

- connection:

​	将多个目标物(如回形针)组成的一个整体切割成多个(数组)，得到回形针数组

- fill_up_shape

  根据自定义的特征进行填充

- select_shape

  缩小目标范围，去除不相干内容

- area_center

- dev_desplay

  展示指定的图像



## 备注

1. 图像类型数组，下标从1开始，且只能通过算子(select_obj)一个个读取