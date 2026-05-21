---
title: "在macOS系统中安装三拼输入法"
date: 2026-05-18 10:30:01 +0800
layout: single
toc: true
toc_label: "安装步骤"  # 自定义目录的标题名称（可选）
toc_icon: "cog"       # 自定义目录标题前的图标（可选）
sidebar:
  nav: "docs"
---

### 1 安装须鼠管

打开中州韵输入法引擎网站，[下载安装须鼠管][Squirrel]

### 2 打开用户文件夹

点击 macOS 右上角状态栏的**鼠须管图标**。<br>
在下拉菜单中选择 **「⚙️ 设置...」**（或「用户设定」）。<br>
打开 Finder 窗口，该目录即为用户配置文件夹，路径通常为 `~/Library/Rime`。

### 3 放入三拼输入法的数据文件

[打开三拼输入法仓库][three]，将其中的数据文件放入用户文件夹

![three](/assets/images/download/macos/three.png)

### 4 修改配置

在用户文件夹中，检查是否存在名为 **`default.custom.yaml`** 的文件。如果没有，请手动新建一个文本文档并重命名为此文件名。<br>
用文本编辑器（如自带的“文本编辑”或 VS Code）打开 `default.custom.yaml`，并在文件中添加以下代码：

```yaml
patch:
  "schema_list/@0":
    schema: three
```

> **⚠️ 注意**：YAML 格式对空格极其敏感，`patch:` 下方必须缩进（建议使用 2 个空格），请勿使用 Tab 键。

### 5 重新部署鼠须管

再次点击 macOS 右上角状态栏的鼠须管图标。<br>
点击 「⟲ 重新部署」（或「部署」）。<br>
稍等几秒钟，当右上角图标闪烁并恢复常态后，代表部署成功。<br>
按下快捷键 ``Ctrl + ` ``(在键盘左上角，数字1左边) ，在弹出的方案选单里，切换到三拼输入法，即可完成安装！

[Squirrel]: https://rime.im/download/
[three]: https://github.com/ChineseInputMethod/three
