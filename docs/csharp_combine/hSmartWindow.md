---
weight: 1
title: "hSmartWindow使用"
date: 2020-12-8
---

# hSmartWindow使用

## 提醒

若将halcon的dll文件拷贝到项目的`bin/debug`目录，需要同时拷贝以下三个文件， 

`halcon.dll, hcanvas.dll`(在halcon安装目录bin下的x64-win64目录)

`halcondotnet.dll`(在halcon安装目录bin下的dotnet35目录)

## 原因

C#项目的`bin/debug`目录下有halcon.dll文件时，其优先级高于halcon在系统中的安装路径下的halcon.dll，

该halcon.dll会引用同目录的其他dll文件，若缺失，则会报错(提示缺失某dll)。

## 排查技巧

1. 将halcon安装目录`bin/x64-win64`下的所有dll文件都拷贝到C#项目的`bin/debug`目录；
2. 运行c#项目，使其能正常执行；
3. 在c#项目运行状态下，删除C#项目的`bin/debug`目录下拷贝的所有dll文件，同时忽略无法删除部分；
4. 最终剩下的无法删除的dll文件，即是可能需要的dll文件；
5. 再一个个删除剩下的dll文件，运行目录下的exe文件，若报错，说明刚删除的dll文件是必要文件。