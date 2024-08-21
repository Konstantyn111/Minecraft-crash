# 🌟 Java 8 安装与Minecraft使用指南 🌟

## 🚀 简介

Java 8是Java语言的里程碑版本，它通过引入流式处理、lambda表达式等特性，极大提升了开发效率和代码质量。本教程将指导您在Windows操作系统上安装Java 8，并确保其与Minecraft 1.0至1.16版本兼容。

## 📋 前提条件

- 至少128MB内存（JRE 124MB，Java Update 132MB）
- 处理器速度至少266MHz
- 稳定浏览器（如IE 9+，Firefox）
- 稳定网络连接以下载Java安装包

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
- 点击“新建”，然后输入Java的安装路径下的“bin”目录路径，例如：`C:\Program Files\Java\jdk1.8.0_XXX\bin`（XXX为具体版本号）。
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

完成上述步骤后，你应已成功安装Java 8并为Minecraft创建了理想的运行环境。

## ⚠ 注意

- 根据Java和Windows版本，安装步骤可能有所不同。
- 本教程基于Java 8和Windows 11编写，其他环境可能需调整。
- 请确保所有软件的安装路径**不包含中文字符**！以避免潜在的访问异常。

请根据实际安装包和操作系统进行相应调整。
