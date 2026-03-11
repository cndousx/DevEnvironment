# Windows下端口被占用

> 有些时候端口不一定是被其他程序占用，而是被 Windows 系统内核（通常是 Hyper-V 或 WinNAT 服务）将端口划入了“动态保留端口范围”，禁止任何用户态程序（包括 Docker）绑定它

1. 查看被系统保留（Excluded）的端口范围

```powershell
netsh interface ipv4 show excludedportrange protocol=tcp
```

2. 重置 WinNAT 服务，重启该服务通常会重新计算保留端口范围，从而释放指定端口

```powershell
sudo net stop winnat && sudo net start winnat
```
