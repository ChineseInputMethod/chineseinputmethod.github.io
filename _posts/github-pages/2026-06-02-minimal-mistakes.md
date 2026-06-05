---
title: "clone remote_theme"
date: 2026-06-02T12:00:00+08:00
categories:
  - GitHub-Pages
tags:
  - SSH
  - Minimal-Mistakes
toc: true
toc_label: "克隆远程主题"  # 自定义目录的标题名称（可选）
toc_icon: "tools"       # 自定义目录标题前的图标（可选）
---

#### 1 安装Git
```bash
sudo apt update
sudo apt install git -y
git -v
```
#### 2 配置Git身份信息
```bash
git config --global user.name "yourname"
git config --global user.email "your_email@example.com"
```
#### 3 生成SSH密钥
```bash
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```
#### 4 查看并复制公钥
```bash
cat ~/.ssh/id_rsa.pub
```
#### 5 将公钥添加到GitHub
{% capture notice-2 %}
* 登录网页版 GitHub，点击右上角头像 -> 选择 Settings
* 在左侧菜单栏找到并点击 SSH and GPG keys
* 点击右上角的 New SSH key
* Title 随便填一个名字（比如 My Laptop），Key 粘贴你刚刚复制的全部内容，点击 Add SSH key 保存
{% endcapture %}
<div class="notice">
  {{ notice-2 | markdownify }}
</div>
#### 6 测试SSH连接
```bash
ssh -T git@github.com
```
#### 7 使用SSH clone远程主题
```bash
git clone git@github.com:你的用户名/你的仓库名.git
```
#### 8 本地调试远程主题
```bash
cd 你的仓库名
bundle install
bundle exec jekyll serve
```
