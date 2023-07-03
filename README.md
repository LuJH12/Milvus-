# Milvus-安装
本教程主要是面对Milvus在`Window11`下安装，使用docker进行下载。

# 安装Docker
由于我们要使用docker来安装Milvus，所以我们得先安装Docker。步骤如下：

## 检查电脑是否开机虚拟化功能
打开控制面板的**启用或关闭 Windows 功能**，并勾选下列红框中的内容。在选择后，需要重启电脑生效。
![2f27142579ba440242dfacf7cbe9218](https://github.com/LuJH12/Milvus-/assets/78155731/cc407c5d-e446-46af-bae0-410489fe933d)

## 安装WSL2
1. 在`开始`菜单中打开`powershell`(已管理员身份打开)
2. 运行以下命令启用 WSL 功能：`dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart`
3. 运行以下命令启用虚拟机功能：`dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart`
4. 从以下链接下载适用于 Windows 11 的 Linux 内核更新包：`https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi`，并双击安装。
5. 重启电脑
6. 设置 WSL 2 为默认版本：打开 PowerShell，运行以下命令以设置 WSL 2 为默认版本：`wsl --set-default-version 2 `
至此，我们可以开始安装Docker了

##
在此链接下载Docker Desktop安装包[Docker Desktop官网地址](https://www.docker.com/products/docker-desktop/)

待更新。。。
