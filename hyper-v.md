要关闭或启动 Hyper-V，可以按照以下方法进行操作。

## 1. 关闭 Hyper-V
关闭 Hyper-V 有两种方法：禁用 Hyper-V 功能 或 使用命令行临时关闭。

### 方法一：通过 "Windows 功能" 禁用 Hyper-V
1. 打开 "Windows 功能"：

    - 按 Win + R 打开运行窗口，输入 optionalfeatures 并按回车。
2. 禁用 Hyper-V：

    - 在弹出的 "Windows 功能" 窗口中，找到 Hyper-V。
    - 取消选中 Hyper-V 及其子选项（"Hyper-V 平台" 和 "Hyper-V 管理工具"）。
    - 点击 确定 并重启计算机。

这样将完全关闭并禁用 Hyper-V 功能。

### 方法二：使用命令行临时禁用 Hyper-V
你可以通过命令行工具在不完全卸载的情况下临时关闭 Hyper-V。

1. 打开 PowerShell 或 CMD（以管理员身份运行）。

2. 输入以下命令禁用 Hyper-V：
```
bcdedit /set hypervisorlaunchtype off
```
3. 重启计算机。

这将临时禁用 Hyper-V。你可以在需要时重新启用它。

## 2. 启动 Hyper-V
如果你之前关闭了 Hyper-V，你可以通过以下方法重新启用它。

### 方法一：通过 "Windows 功能" 启用 Hyper-V
1. 打开 "Windows 功能"：

    - 按 Win + R 打开运行窗口，输入 optionalfeatures 并按回车。
2. 启用 Hyper-V：

    - 在弹出的 "Windows 功能" 窗口中，找到 Hyper-V，并勾选它和所有子选项（"Hyper-V 平台" 和 "Hyper-V 管理工具"）。
    - 点击 确定，然后重启电脑。
### 方法二：使用命令行重新启用 Hyper-V
1. 打开 PowerShell 或 CMD（以管理员身份运行）。

2. 输入以下命令启用 Hyper-V：
```
bcdedit /set hypervisorlaunchtype auto
```
3. 重启计算机。

这样 Hyper-V 就会重新启用。

## 总结
- 禁用/启用 Hyper-V 可以通过 "Windows 功能" 或命令行完成。
- 使用 bcdedit 命令可以临时禁用或重新启用 Hyper-V，而不需要完全卸载。