# Windows PE

|本期版本|上期版本
|:---:|:---:
`Thu Feb 29 22:38:20 CST 2024` | -

## Command

**Env**

```bash
PE=C:\WinPE_amd64
mount=C:\WinPE_amd64\mount
cab=C:\Program Files\Windows Kits\10\Assessment and Deployment Kit\Windows Preinstallation Environment\amd64\WinPE_OCs
bootwim=C:\WinPE_amd64\media\sources\boot.wim
```

```bash
copype amd64 C:\winpe_amd64
Dism /Mount-Image /ImageFile:"C:\WinPE_amd64\media\sources\boot.wim" /index:1 /MountDir:"C:\WinPE_amd64\mount"

Dism /Add-Package /Image:"C:\WinPE_amd64\mount" /PackagePath:"C:\Program Files (x86)\Windows Kits\10\Assessment and Deployment Kit\Windows Preinstallation Environment\amd64\WinPE_OCs\WinPE-WMI.cab"

Dism /Add-Package /Image:"C:\WinPE_amd64\mount" /PackagePath:"C:\Program Files (x86)\Windows Kits\10\Assessment and Deployment Kit\Windows Preinstallation Environment\amd64\WinPE_OCs\WinPE-SecureStartup.cab"

DISM /image:c:\winpe_amd64\mount /Cleanup-image /StartComponentCleanup

dism /unmount-image /mountdir:c:\winpe_amd64\mount /commit
dism /export-image /sourceimagefile:c:\winpe_amd64\media\sources\boot.wim /sourceindex:1 /DestinationImageFile:c:\winpe_amd64\mount\boot2.wim
Del c:\winpe_amd64\media\sources\boot.wim
Copy c:\winpe_amd64\mount\boot2.wim c:\winpe_amd64\media\sources\boot.wim

MakeWinPEMedia /iso C:\winpe_amd64 D:\winpe_amd64.iso
```

## [关于在 Windows PE 中运行 Windows 安装程序的说明](https://learn.microsoft.com/zh-cn/windows-hardware/manufacture/desktop/winpe-intro?view=windows-11#notes-on-running-windows-setup-in-windows-pe)

## [Hex-Railty的个人空间-Hex-Railty个人主页-哔哩哔哩视频](https://space.bilibili.com/495022394)

* [【从…到…】#0：Windows ADK的安装](https://www.bilibili.com/video/BV1ua41117RE)
* [【从…到…】#1：最基本Windows PE ISO的导出与测试！](https://www.bilibili.com/video/BV1K34y1C7hK)
* [[无后期处理] #1.5：将WinPE写入USB驱动器](https://www.bilibili.com/video/BV1iS4y1r7xK)
* [[从…到…] #1.75：实体机上从USB驱动器启动WinPE](https://www.bilibili.com/video/BV1DY411g7yD)
* [[从…到…] #2.5：抢救性补充说明！](https://www.bilibili.com/video/BV1Pi4y1S7AX)
* **[[从…到…] #2：自定义WinPE](https://www.bilibili.com/video/BV1d44y1V79a)**


## Ref

* [Copype 命令行选项 | Microsoft Learn](https://learn.microsoft.com/zh-cn/windows-hardware/manufacture/desktop/copype-command-line-options?view=windows-11)
* [Makewinpemedia 命令行选项 | Microsoft Learn](https://learn.microsoft.com/zh-cn/windows-hardware/manufacture/desktop/makewinpemedia-command-line-options?view=windows-11)
* [WinPE：装载和自定义 | Microsoft Learn](https://learn.microsoft.com/zh-cn/windows-hardware/manufacture/desktop/winpe-mount-and-customize?view=windows-11)
* [关于在 Windows PE 中运行 Windows 安装程序的说明](https://learn.microsoft.com/zh-cn/windows-hardware/manufacture/desktop/winpe-intro?view=windows-11#notes-on-running-windows-setup-in-windows-pe)