---
weight: 1
title: "使用VisualStudio开发halcon的配置"
date: 2020-12-8
---

# 使用VisualStudio开发halcon的配置

### 步骤
1. 在项目属性中，_生成代码_ 选项不勾选[**首选32位**]；**※重要**
2. 在Form设计界面，打开**工具箱**， 右键选择**选择项**， 点击**浏览**，勾选halcon安装目录下的`bin/dotnet35`目录下的halcondotnet.dll文件；（此时可以在工具箱中拖拽使用hWindowControl控件了)
3. 添加项目引用，选择halcondotnet.dll文件；（后缀是xl.dll的文件，用于大分辨率相机，如2000万像素以上）
4. (可选项)，若想不依赖系统中的安装程序halcon，需要将相关dll文件放入c#项目的`bin/debug`目录下。(exe文件目录) 
5. (可选项)，Halcon安装目录下的`misc`目录中，有VS插件`HALCON1911ProgressVariableInspect.vsix`，双击安装后可以在VisualStudio中右键Halcon类型变量，添加到插件监控中。

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

  

  