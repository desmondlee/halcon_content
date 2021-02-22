---
date: 2021-01-19
title: "border_shape_models"
---

形状模板可能与图像边缘相交，为了确保在这种情况下也能定位到，需要开启该功能：
```
set_system('border_shape_models', 'true')
```