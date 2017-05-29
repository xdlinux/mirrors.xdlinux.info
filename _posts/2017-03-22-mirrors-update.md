---
layout: post
title: "软件源同步更新"
date: 2017-03-22 15:00:00 +0800
categories: news
description: Ubuntu 和 Debian 源同步方式由 debmirror 改为 rsync
---

#### changelog

1. `Ubuntu` 和 `Debian` 源同步方式由 `debmirror` 改为 `rsync`

### Ubuntu

* 收录版本：所有 Ubuntu 当前支持的版本，包括开发版，具体版本见 [https://wiki.ubuntu.com/Releases](https://wiki.ubuntu.com/Releases)
* 收录架构：`x86_64`, `i386`
* 上游：[mirrors.tuna.tsinghua.edu.cn/ubuntu/](https://mirrors.tuna.tsinghua.edu.cn/ubuntu/)
* 使用方式

```
以 xenial (16.04 LTS) 为例， 编辑 /etc/apt/sourse.list
替换为以下内容（请做好相应备份）

deb http://mirrors.xdlinux.info/ubuntu/ xenial main restricted universe multiverse
deb-src http://mirrors.xdlinux.info/ubuntu/ xenial main restricted universe multiverse

deb http://mirrors.xdlinux.info/ubuntu/ xenial-security main restricted universe multiverse
deb-src http://mirrors.xdlinux.info/ubuntu/ xenial-security main restricted universe multiverse

deb http://mirrors.xdlinux.info/ubuntu/ xenial-updates main restricted universe multiverse
deb-src http://mirrors.xdlinux.info/ubuntu/ xenial-updates main restricted universe multiverse

deb http://mirrors.xdlinux.info/ubuntu/ xenial-backports main restricted universe multiverse
deb-src http://mirrors.xdlinux.info/ubuntu/ xenial-backports main restricted universe multiverse

deb http://mirrors.xdlinux.info/ubuntu/ xenial-proposed main restricted universe multiverse
deb-src http://mirrors.xdlinux.info/ubuntu/ xenial-proposed main restricted universe multiverse
```

### Debian

* 收录版本：`oldstable`, `stable`, `testing`, `unstable (sid)`
* 收录架构：`x86_64`, `i386`
* 去除了 `kfreebsd` 和 `hurd` 的支持
* 上游：[mirrors.tuna.tsinghua.edu.cn/debian/](https://mirrors.tuna.tsinghua.edu.cn/debian/)
* 使用方式

```
以 jessie (Debian 8) 为例， 编辑 /etc/apt/sourse.list
将**除 security 之外**的源地址替换为以下内容（请做好相应备份）

deb http://mirrors.xdlinux.info/debian/ jessie main non-free contrib
deb http://mirrors.xdlinux.info/debian/ jessie-proposed-updates main non-free contrib
deb-src http://mirrors.xdlinux.info/debian/ jessie main non-free contrib
deb-src http://mirrors.xdlinux.info/debian/ jessie-proposed-updates main non-free contrib
```

#### 欢迎测试、反馈

* [feedback@xdlinux.info](mailto:feedback@xdlinux.info)
* QQ群：`226198461` 西电开源社区

