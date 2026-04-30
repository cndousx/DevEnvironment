```powershell
PowerShell 7.6.1
PS C:\Users\dousx> wsl --list --verbose
  NAME              STATE           VERSION
* Ubuntu-24.04      Running         2
  docker-desktop    Running         2
  Ubuntu-26.04      Stopped         2
PS C:\Users\dousx> wsl --terminate Ubuntu-26.04
操作成功完成。
PS C:\Users\dousx> wsl --unregister Ubuntu-26.04
正在注销。
操作成功完成。

PS C:\Users\dousx> wsl --list --verbose
  NAME              STATE           VERSION
* Ubuntu-24.04      Running         2
  docker-desktop    Running         2
PS C:\Users\dousx>
```

![image-20260430154904137](https://cruder-figure-bed.oss-cn-beijing.aliyuncs.com/markdown/2026/04/30/15-49-04-408-df74a77a386c4654a503200402ad4cb1.png)