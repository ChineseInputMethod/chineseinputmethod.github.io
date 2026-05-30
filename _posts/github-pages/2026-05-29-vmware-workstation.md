---
title: "安装VMware Workstation"
date: 2026-05-29T16:00:00+08:00
categories:
  - GitHub Pages
tags:
  - VMware Workstation
  - 汉化
link: https://broadcom.com
---

VMware Workstation的升级十分简单，点击更新窗口的更新说明

![update](/assets/images/github-pages/vmware-workstation/update.png)

在打开的网页中，点击下载

![download](/assets/images/github-pages/vmware-workstation/download.png)

打开协议页面，然后回到当前页面，选中同意

![term](/assets/images/github-pages/vmware-workstation/term.png)

下载安装后，将[汉化包][zh_CN]中的`zh_CN`文件夹，拷贝到安装目录的`messages`文件夹

在快捷方式后添加` --locale zh_CN`，即可完成汉化

```
"C:\Program Files\VMware\VMware Workstation\vmware.exe" --locale zh_CN
```

[zh_CN]: https://github.com/Kuroba-Sayuki/VMware-Workstation-Chinese-Localization
