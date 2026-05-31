---
title: "在VMware中，安装 Ubuntu 26H1"
date: 2026-05-30T16:00:00+08:00
categories:
  - GitHub Pages
tags:
  - Ubuntu
  - open-vm-tools
---

> <a href="https://ubuntu.com/download">下载Ubuntu</a>

安装完成后，安装VMware驱动

```bash
sudo apt update
sudo apt install open-vm-tools open-vm-tools-desktop -y
```
设置本地时间

```bash
timedatectl set-local-rtc 1 --adjust-system-clock
```
