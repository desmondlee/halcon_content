---
weight: 1
title: "Halcon数据类型"
date: 2020-12-8
---

# Halcon的数据类型



## 命名规范

Halcon导出的图像变量类型是HObject，简称 ho；导出的控制变量类型是HTuple，简称 hv。

### 图像类型的使用步骤

1. 用GenEmptyObj初始化图像变量，或产生一个非空的图像变量；
2. 在更新图像变量的内容前，用Dispose释放资源；
3. 使用图像变量；
4. 图像变量生命周期结束时，用Dispose释放资源。(C#中有GC垃圾回收机制，不强制Dispose；但C++中必须)

> 如果不及时用Dispose释放资源，可能会导致内存泄漏。



## C#与Halcon数据间转换

1. tuple变量赋值给C#变量：

   ```
   csharp_int = halcon_int[0].I   (英文字母i 的大写，表示int)
   
   csharp_real = halcon_real[0].D (英文字母d的大写，表示double)
   
   csharp_string = halcon_string[0].S (英文字母s的大写，表示string)
   ```

2. C#变量赋值给tuple变量：

   ```
   halcon_int = csharp_int * 2;  (隐式转换)
   halcon_int = (HTuple)(csharp_int * 2) (显示强制转换)
   halcon_int = new HTuple(csharp_int * 2)
   ```

   