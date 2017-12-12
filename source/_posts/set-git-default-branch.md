---
title: 设置git默认分支
date: 2017-12-09 14:43:37
categories: "命令"
tags:
  - git命令
---
提交将会出现在github贡献图中,必须满足3个条件,其中一个是**提交必须在仓库的默认分支中,通常是master分支.**
git branch --set-upstream-to=origin/dev dev
