# 列出已经安装的wsl及其版本

```
wsl --list --verbose
```

或者

```
wsl -l -v
```


## 步骤 1：确保系统支持 WSL 2

首先，确认你的系统支持 WSL 2。WSL 2 需要 Windows 10 版本 1903 或更高版本，并且系统内核版本为 18362 或更高。

## 步骤 2：安装 WSL 2 内核组件
如果你还没有安装 WSL 2 内核组件，按照以下步骤进行：

打开 PowerShell（以管理员身份运行）。

执行以下命令，安装 WSL 2 的内核组件：
```
wsl --update
```
安装成功后，你可以通过以下命令设置 WSL 2 为默认版本（可选）：
```
wsl --set-default-version 2
```

## 步骤 3：将特定的 WSL 1 发行版转换为 WSL 2
要将特定的 Linux 发行版从 WSL 1 转换到 WSL 2，执行以下命令：

打开 PowerShell 或 CMD。

输入以下命令：
```
wsl --set-version <发行版名称> 2
```
例如，如果你要将 Ubuntu 切换到 WSL 2：
```
wsl --set-version Ubuntu-22.04 2
```

wsl.exe --install --no-distribution 安装可选组件虚拟机平台

```
正在安装 Windows 可选组件: VirtualMachinePlatform

部署映像服务和管理工具
版本: 10.0.19041.3636

映像版本: 10.0.19045.4780

启用一个或多个功能
[==========================100.0%==========================]
操作成功完成。
请求的操作成功。直到重新启动系统前更改将不会生效。
```

# VMware WorkStation兼容性
打开了Hyper-V后，会影响VMware需要关闭CPU配置里的虚拟化引擎
1. 虚拟化IntelVT-x/EPT或AMD-V/RVI(V)
2. 虚拟化CPU性能计数器(U)

