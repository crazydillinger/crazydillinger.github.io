---
title: Cmder:windows上的完美的控制台模拟器
---

#### 目录

- cmder
- 安装包
- 环境变量
- 右键菜单
- 添加命令
- 默认路径
- 中文乱码

### cmder

cmder是一个增强命令行工具,不仅可以试用windows下所有命令,还可以使用linux,shell命令

More info: [Crmder](http://cmder.net/)

### 环境变量

把crmder的home目录路径放到path中,即可以在win + R中搜索到exe程序

> 如把D:\program\cmder放到path变量中

### 右键菜单
进入cmder的根目录,执行命令

```
cd cmder
Cmder.exe /REGISTER ALL
```

### 添加命令

```
l=ls --show-control-chars 
la=ls -aF --show-control-chars 
ll=ls -alF --show-control-chars 
ls=ls --show-control-chars -F
```

### 默认路径

打开设置,选择**Startup-Task**,修改**{cmd::cmder}**
>cmd /k "%ConEmuDir%\..\init.bat"  -new_console:d:目录名

### 中文乱码

打开设置,选择**Startup-Task**,修改environment.
>set PATH=%ConEmuBaseDir%\Scripts;%PATH%
set LANG=zh_CN.UTF8
