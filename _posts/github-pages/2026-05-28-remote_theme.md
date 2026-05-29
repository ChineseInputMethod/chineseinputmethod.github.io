---
title: "在GitHub Pages上架设网站最简单的方法"
date: 2026-05-28T16:00:00+08:00
categories:
  - GitHub Pages
tags:
  - remote_theme
  - minimal-mistakes
---

GitHub Pages的官方文档实在让人一言难尽，说的内容都对，但是新手看了大体都是蒙的

其实使用远程主题，可以[一键生成][minimal-mistakes]，开箱即用

![remote_theme](/assets/images/github-pages/remote_theme/minimal-mistakes.png)

本站就是折腾了很久，最后选择了这个最简单的方法

本地主题和远程主题，主要有三个地方不同：

一、本地主题包含了所有文件，远程主题只包含了必要的文件

二、本地主题必须构建环境，以保证插件工作正常，远程主题是GitHub维护的

三、本地主题包含工作流文件，远程主题是push后，GitHub自动部署的

[minimal-mistakes]: https://github.com/mmistakes/mm-github-pages-starter/generate
