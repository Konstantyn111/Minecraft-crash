# 🌟 Java 8 安装与Minecraft使用指南 🌟

## 🚀 简介

Java 8是Java语言的里程碑版本，它通过引入流式处理、lambda表达式等特性，极大提升了开发效率和代码质量。本教程将指导您在Windows操作系统上安装Java 8，并确保其与Minecraft 1.0至1.16版本兼容。

## 📋 前提条件

- 操作系统：Java 16支持多种操作系统，包括但不限于Windows 10/11、macOS（最新版本）、Linux（多个发行版）。

- 处理器：至少1 GHz或更快的处理器。

- 内存：至少2 GB的RAM（对于32位系统）或4 GB的RAM（对于64位系统）。

- 硬盘空间：至少需要1.5 GB的可用硬盘空间来安装JDK。

- 图形用户界面：如果使用图形安装程序，需要支持至少1024x768的分辨率。

- 网络连接：在下载JDK安装包时需要网络连接。

权限：安装Java可能需要管理员权限或root权限，具体取决于你的操作系统和安装方式。
## 📥 步骤1：下载Java 8

点击以下链接下载Java 8安装包：
	[点击下载Java 8](https://download.bell-sw.com/java/8u422+6/bellsoft-jdk8u422+6-windows-amd64.msi)

## 🔧 步骤2：安装Java 8

1. 双击安装程序启动向导。

2. 点击“Next”进入下一步。
   ·![1](https://github.com/Konstantyn111/Minecraft-crash/blob/main/img/java/1.png)

3. **确保安装路径不包含中文字符**，建议使用默认路径或更改至无中文的可访问路径。

   ![2](https://github.com/Konstantyn111/Minecraft-crash/blob/main/img/java/2.png)

4. 点击“Install”开始安装。

   ![3](https://github.com/Konstantyn111/Minecraft-crash/blob/main/img/java/3.png)

## 🔍 步骤3：验证Java 8安装

1. 使用win+R打开运行窗口输入“cmd”,点击”确定“

   ![4](https://github.com/Konstantyn111/Minecraft-crash/blob/main/img/java/4.png)

2. 打开CMD，输入`java -version`检查安装。

3. 如果`java -version`没有显示Java版本，请设置环境变量（见下文）。

3. 确保Minecraft设置为使用Java 8。

### 设置环境变量

- 右键点击“此电脑”或“计算机”，选择“属性”。
- 在打开的窗口中，点击“高级系统设置”。
- 在“系统属性”窗口中，点击“环境变量”。
- 在“系统变量”中找到“Path”变量，选择它并点击“编辑”。
- 点击“新建”，然后输入Java的安装路径下的“bin”目录路径，例如：`C:\Program Files\Java\jdkXXX\bin`（XXX为版本号）。
- 点击“确定”保存设置并关闭所有打开的窗口。

## 🎮 使用HMCL和PCL运行Minecraft

### HMCL安装
- **请勿将HMCL放置在中文路径或可能导致访问异常的路径**，例如C盘用户文件夹。
- [插入HMCL图片]
- 描述HMCL的安装和配置过程。

### PCL安装
- **请勿将PCL放置在中文路径或可能导致访问异常的路径**，例如C盘用户文件夹。
- [插入PCL图片]
- 描述PCL的安装和配置过程。

## 🎉 结语

完成上述步骤后，您应已成功安装Java 8并为Minecraft创建了理想的运行环境。记得更新Java以确保游戏兼容性和系统安全。

## ⚠ 注意

- 根据Java和Windows版本，安装步骤可能有所不同。
- 本教程基于Java 8和Windows 11编写，其他环境可能需调整。
- 请确保所有软件的安装路径**不包含中文字符**！以避免潜在的访问异常。

请根据实际安装包和操作系统进行相应调整。