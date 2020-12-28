---
weight: 1
title: "使用VisualStudio开发halcon的配置"
date: 2020-12-8
---

# 使用VisualStudio开发halcon的配置

### 步骤
1. 在项目属性中，生成代码选项不勾选[**首选32位**]；
2. 在Form设计界面，打开**工具箱**， 右键选择**选择项**， 点击**浏览**，勾选halcon安装目录下的bin目录下的dotnet35目录下的halcondotnet.dll文件；（此时可以在工具箱中拖拽使用hWindowControl控件了)
3. 添加项目引用，选择halcondotnet.dll文件；（后缀是xl.dll的文件，用于大分辨率相机，如2000万像素以上）
4. (可选项)，若想不依赖系统中的安装程序halcon，需要将相关dll文件放入c#项目的bin-debug目录下。(exe文件目录)

### 实例

[项目代码文件下载](http://qn.halcon.lizhenguo.cn/attachment/WindowsFormsApp5.zip)

> ps, vs版本为2017社区版



## 切换版本

1. 更换C#项目资源管理器，引用列表中的halcondotnet引用文件；
2. 在工具箱、项目中，都重新引入最新的halcondotnet.dll动态库文件；
3. 重新拖拽生成hWindowControl窗口控件。



## 快捷键

- 格式化代码

  ```
  ctrl+k+f
  ```

  

  