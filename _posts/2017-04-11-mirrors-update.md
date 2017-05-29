---
layout: post
title: "软件源同步更新"
date: 2017-04-11 10:20:00 +0800
categories: news
description: kali 和 deepin 同步方式由 debmirror 改为 rsync
---

#### changelog

1. `kali` 和 `deepin` 同步方式由 `debmirror` 改为 `rsync`
2. 完全弃用 debmirror
  * 优点：
    1. 可以按版本、架构筛选 deb 发行版软件源。
    2. 校验签名，Hash
  * 缺点：
    1. 软件源结构调整后导致无法完成同步（需要修改 debmirror）。
    2. 解析 Release 速度慢。
3. 目前的解决方案
  * rsync + filter （粗粒度过滤，易过滤架构，难过滤版本）

Q: 为什么要过滤，不全部同步？  
A: `x86_64` 之外的架构使用很少，带宽有限，且行且珍惜。（并且 ipv4 流量有限，所以仅对内网服务）。

Q: 同步失败一般是什么原因？  
A: some files vanished before they could be transferred. （会考虑把失败原因显示在主页）。

### kali

* 说明：Kali Linux 软件源
* 收录架构：`x86_64`, `i386`
* 上游：[mirrors.tuna.tsinghua.edu.cn/kali/](https://mirrors.tuna.tsinghua.edu.cn/kali/)
* 使用方式

```
编辑 /etc/apt/sources.list 文件, 修改为：

deb https://mirrors.xdlinux.info/kali kali-rolling main non-free contrib
deb-src https://mirrors.xdlinux.info/kali kali-rolling main non-free contrib
```

### deepin

* 说明：Deepin Linux 软件源
* 收录架构：`x86_64`, `i386`
* 上游：[mirrors.tuna.tsinghua.edu.cn/deepin/](https://mirrors.tuna.tsinghua.edu.cn/deepin/)
* 使用方式

```
编辑 /etc/apt/sources.list，修改为

deb http://mirrors.xdlinux.info/deepin unstable main contrib non-free
deb-src http://mirrors.xdlinux.info/deepin unstable main contrib non-free
```

#### 欢迎测试、反馈

* [feedback@xdlinux.info](mailto:feedback@xdlinux.info)
* QQ群：`226198461` 西电开源社区

