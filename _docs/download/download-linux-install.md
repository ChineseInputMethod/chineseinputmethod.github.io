---
title: "在macOS系统中安装三拼输入法"
date: 2026-05-18 10:30:02 +0800
layout: single
toc: true
toc_label: "安装步骤"  # 自定义目录的标题名称（可选）
toc_icon: "cog"       # 自定义目录标题前的图标（可选）
sidebar:
  nav: "docs"
---

在Linux中安装三拼输入法的步骤基本相同，[打开中州韵输入法引擎][linux]，查看Linux 发行版和输入法框架的安装说明。<br>
本文以Ubuntu的ibus框架举例，来说明如何安装。

### 1 安装ibus-rime

打开终端，执行以下命令安装 `ibus-rime`

```bash
sudo apt update
sudo apt install ibus-rime
```

然后重启 IBus服务

```bash
ibus restart
```

### 2 添加输入源

打开系统 设置 (Settings) -> 点击 键盘 (Keyboard)<br>
找到 输入源 (Input Sources)，点击下方的 + 添加输入源(A)<br>
在弹出的窗口中点击 汉语 (Chinese)<br>
选中 中文 (Rime)，点击右上角的 添加 (Add)

![ibus](/assets/images/download/linux/ibus.png)

### 3 初始部署Rime 

点击右上角输入法图标，在弹出菜单中，切换到中文（Rime），等待几秒钟完成Rime的初始部署

![rime](/assets/images/download/linux/rime.png)

### 4 添加三拼输入法

打开rime用户文件夹<br>
在ibus框架中，rime的用户文件夹，通常为`~/.config/ibus/rime`

[下载数据文件][three]，解压后将数据文件放入用户文件夹

![three](/assets/images/download/macos/three.png)

### 5 修改配置

在rime用户文件夹中，检查是否存在名为 **`default.custom.yaml`** 的文件<br>
如果没有，请手动新建一个文本文档并重命名为此文件名。<br>
用文本编辑器（如自带的“文本编辑”或 VS Code）打开 `default.custom.yaml`，并在文件中添加以下代码：

```yaml
patch:
  "schema_list/@0":
    schema: three
```

> **⚠️ 注意**：YAML 格式对空格极其敏感，`patch:` 下方必须缩进（建议使用 2 个空格），请勿使用 Tab 键。

### 6 重新部署

再次点击 右上角状态栏的輸入法图标。<br>
在弹出菜单中，点击 「⟲ 重新部署」（或「部署」）。

![deploy](/assets/images/download/linux/deploy.png)

按下快捷键 ``Ctrl + ` ``(在键盘左上角，数字1左边) ，在弹出的方案选单里，切换到三拼输入法，即可完成安装！

![three](/assets/images/download/linux/three.png)

{:target="_blank" rel="noopener noreferrer"}
[linux]: https://rime.im/download/

{:target="_blank" rel="noopener noreferrer"}
[three]: https://github.com/ChineseInputMethod/three/archive/refs/heads/main.zip
