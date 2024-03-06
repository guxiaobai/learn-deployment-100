# learn-deployment-100

* `CTRL+SHIFT+F3`: [将 Windows 启动至审核模式或 OOBE](https://learn.microsoft.com/zh-cn/windows-hardware/manufacture/desktop/boot-windows-to-audit-mode-or-oobe?view=windows-11)
* `Shift+F10`: [Windows 安装：使用 MBR 或 GPT 分区形式进行安装](https://learn.microsoft.com/zh-cn/windows-hardware/manufacture/desktop/windows-setup-installing-using-the-mbr-or-gpt-partition-style?view=windows-11)
* [WDS部署-制作无人自动应答文件（BIOS/UEFI）附视频](https://blog.csdn.net/u014588173/article/details/133276781 )


## 在下莫老师的个人空间-在下莫老师个人主页-哔哩哔哩视频

* [一键重装的版本答案？利用Ventoy+应答脚本，手搓一个无人值守系统安装U盘](https://www.bilibili.com/video/BV12w411w7ju)
* [一次装机100台！iVentoy，新一代PXE网启服务器使用指南](https://www.bilibili.com/video/BV1hP411e7HD/)


## Misc

* [imagex工具整合window11的wim镜像](https://blog.csdn.net/u010080562/article/details/120622554)

> DISM 取代了數種部署工具，包括 PEimg、Intlcfg、ImageX 和套件管理員。

* [DISM - 部署映像服務與管理](https://learn.microsoft.com/zh-tw/windows-hardware/manufacture/desktop/dism---deployment-image-servicing-and-management-technical-reference-for-windows?view=windows-11)
* [DISM 概述](https://learn.microsoft.com/zh-cn/windows-hardware/manufacture/desktop/what-is-dism?view=windows-11)
* [windows系统查看用户sid](https://www.cnblogs.com/heqiuyu/p/14299560.html)
* [大白狗的封装札记 - 2 基础知识_IT天空](https://www.itsk.com/thread/402224)
* [小鱼儿yr系统 - 专注于系统封装重装系统下载软件分享教程](https://www.yrxitong.com/)


## Command

```bash
net user Administrator /active:Yes

whoami /user
wmic useraccount get name,sid
```