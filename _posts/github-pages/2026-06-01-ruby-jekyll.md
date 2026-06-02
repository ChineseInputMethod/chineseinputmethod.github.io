---
title: "搭建jekyll本地运行环境"
date: 2026-06-01T12:00:00+08:00
categories:
  - GitHub-Pages
tags:
  - ruby
  - jekyll
toc: true
toc_label: "构建jekyll运行环境步骤"  # 自定义目录的标题名称（可选）
toc_icon: "tools"       # 自定义目录标题前的图标（可选）
---

#### 1 安装Ruby
sudo apt update  
sudo apt install make gcc g++  
sudo apt install ruby-dev
{: .notice}

#### 2 配置Gem
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc  
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc  
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc  
source ~/.bashrc
{: .notice--primary}

#### 3 替换RubyGems源
gem sources --add https://gems.ruby-china.com/  
gem sources --remove https://rubygems.org/  
gem sources -l
{: .notice--info}

#### 4 安装jekyll
gem install jekyll bundler  
bundle config set mirror.https://rubygems.org https://gems.ruby-china.com/  
jekyll -v
{: .notice--warning}

#### 5 生成测试网站
jekyll new myblog  
cd myblog  
bundle exec jekyll serve
{: .notice--danger}

#### 6 访问测试网站
http://127.0.0.1:4000
{: .notice--success}
