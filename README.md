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

## 下载并安装Docker Desktop
在此链接下载Docker Desktop安装包[官网地址](https://www.docker.com/products/docker-desktop/)

至此，我们应该就可以正常使用Docker了。

# 在Docker下安装Milvus
下载[milvus-standalone-docker-compose.yml](https://github.com/milvus-io/milvus/releases/download/v2.0.2/milvus-standalone-docker-compose.yml)并手动或使用以下命令将其保存为`docker-compose.yml`。

在想要存放镜像的地方新建一个文件夹，并将该文件放进，且创建创建五个文件夹分命名为，conf、db、logs、pic、volumes、wal。

之后，在该路径下打开命令行窗口，输入`docker-compose up -d`并敲回车，等待安装。

在安装成功后，我们就可以在Docker里面看到了(如果看不到端口号的话，点击一下运行就可以)
![710fec82219d4a905b8052b5e2be6d3](https://github.com/LuJH12/Milvus-install-Window11/assets/78155731/3f2de8a3-541d-4efe-a5dd-e3da05d0dd49)

这个时候我们并不能很方便的可视化看Milvus，我们可以下载一个官方软件Attu来进行可视化。

# 安装Attu
进入[下载地址](https://github.com/zilliztech/attu/releases)，选择合适的安装包。
![48e802231e2ece5da2695e1fc1e5004](https://github.com/LuJH12/Milvus-install-Window11/assets/78155731/1567d7a3-e934-4cda-9569-2744019df932)

在安装完成后，输入Docker里的端口号，点击Connect。
![bf698c8683d311e0d6462e383018acf](https://github.com/LuJH12/Milvus-install-Window11/assets/78155731/5a7b4a98-cb4d-4229-920a-c8610260e0c0)

即可成功的Milvus可视化！
![0aa9ead8b629d859a6cea0426acf123](https://github.com/LuJH12/Milvus-install-Window11/assets/78155731/fc66a40a-07ed-4469-a5eb-c6b9a9995197)






待更新。。。
