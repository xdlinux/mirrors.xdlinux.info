---
layout: post
title: "软件源同步更新"
date: 2017-03-29 11:00:00 +0800
categories: news
description: 新增 debian-security 镜像； debian-multimedia 同步方式由 debmirror 改为 rsync
---

#### changelog

1. 新增 `debian-security` 镜像
2. `debian-multimedia` 同步方式由 `debmirror` 改为 `rsync`

### debian-security

* 说明：debian 软件安全更新源
* 收录版本：`oldoldstable`, `oldstable`, `stable`, `testing`
* 收录架构：`x86_64`, `i386`
* 去除了 `kfreebsd` 和 `hurd` 的支持
* 上游：[mirrors.tuna.tsinghua.edu.cn/debian-security/](https://mirrors.tuna.tsinghua.edu.cn/debian-security/)
* 使用方式

```
以 jessie (Debian 8) 为例， 编辑 /etc/apt/sourse.list
将 security 源地址替换为以下内容（请做好相应备份）

deb http://mirrors.xdlinux.info/debian-security/ jessie/updates main non-free contrib
deb-src http://mirrors.xdlinux.info/debian-security/ jessie/updates main non-free contrib
```

### debian-multimedia

* 说明：debian 第三方多媒体软件源
* 收录版本：`oldstable`, `stable`, `testing`, `unstable (sid)`
* 收录架构：`x86_64`, `i386`
* 去除了 `kfreebsd` 和 `hurd` 的支持
* 上游：[mirrors.tuna.tsinghua.edu.cn/debian-multimedia/](https://mirrors.tuna.tsinghua.edu.cn/debian-multimedia/)
* 使用方式

```
以 jessie (Debian 8) 为例， 编辑 /etc/apt/sourse.list
添加以下内容（请做好相应备份）

deb http://mirrors.xdlinux.info/debian-multimedia/ jessie main non-free
deb-src http://mirrors.xdlinux.info/debian-multimedia/ jessie main non-free
deb http://mirrors.xdlinux.info/debian-multimedia/ jessie-backports main
deb-src http://mirrors.xdlinux.info/debian-multimedia/ jessie-backports main
```

#### 欢迎测试、反馈

* [feedback@xdlinux.info](mailto:feedback@xdlinux.info)
* QQ群：`226198461` 西电开源社区

