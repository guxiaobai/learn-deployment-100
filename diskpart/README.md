# diskpart

|本期版本|上期版本 
|:---:|:---:
`Thu Feb 29 22:21:25 CST 2024` | -

## Ventoy

> `VentoyAutoRun.bat`

```bash
diskpart /s X:\CreatePartitions-UEFI.txt
```

`Partition` | `Size` | `Format`
---|---|---
`ESP` | `300` | `fat32`
`MSR` | `128` | -
`C` | -| `ntfs`



## Ref



* [diskpart | Microsoft Learn](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/diskpart)
* [部署实验室示例脚本 | Microsoft Learn](https://learn.microsoft.com/zh-cn/windows-hardware/manufacture/desktop/oem-deployment-of-windows-desktop-editions-sample-scripts?view=windows-11)