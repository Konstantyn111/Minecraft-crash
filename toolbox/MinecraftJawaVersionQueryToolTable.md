# Minecraft Java相关查询工具表

## Java版本与Minecraft模组兼容性指南

### Java术语解释

- **JVM（Java虚拟机）**: JVM是一个可以执行Java字节码的虚拟计算机。它是Java平台的核心组件，实现了Java语言的运行时环境，使得Java能够实现跨平台的特性。JVM提供了内存管理、垃圾回收和安全性等关键服务。

- **JRE（Java运行环境）**: JRE是Java应用程序的运行时环境，包含了JVM和Java核心类库。它不包含开发工具，是运行Java程序的最小需求。用户在使用Java应用程序时，通常需要安装JRE。

- **JDK（Java开发工具包）**: JDK是面向Java开发者的完整开发环境，包含了JRE、Java编译器（javac）、Java文档生成器（javadoc）、调试器和其他工具。JDK是开发Java应用程序的必需工具。


### Minecraft版本与Java版本对照表

|           Minecraft版本            |                   推荐Java版本                 |
| :--------------------------------: | :--------------------------------------------: |
|            1.0 - 1.11.x            |           推荐Java 8；兼容Java 6/7           |
| 1.12(17w13a) - 1.16.5(1.17-21w18a) | 必须使用Java 8（部分可兼容Java 9以上版本）   |
|       1.17(21w19a) - 1.17.1        |           使用Java 16；部分兼容Java 17          |
|      1.18(1.18-pre2) - 1.20.4      |                 必须使用Java 17                |
|           1.20.5(24w14a)           |                 必须使用Java 21                |
|                                    |                                                |

**注意**: 整合包或有特殊需求的模组请根据作者的要求选择Java版本。原版Minecraft对Java兼容性较强，可以使用推荐版本以上的Java版本启动，但不建议使用过高版本Java启动低版本游戏。

### Java版本与Class File版本对照表

| JDK Version | Class File Version |
|--------------|--------------------|
| Java 1.0     | 45.0               |
| Java 1.1     | 45.3               |
| Java 1.2     | 46.0               |
| Java 1.3     | 47.0               |
| Java 1.4     | 48.0               |
| Java 5       | 49.0               |
| Java 6       | 50.0               |
| Java 7       | 51.0               |
| Java 8       | 52.0               |
| Java 9       | 53.0               |
| Java 10      | 54.0               |
| Java 11      | 55.0               |
| Java 12      | 56.0               |
| Java 13      | 57.0               |
| Java 14      | 58.0               |
| Java 15      | 59.0               |
| Java 16      | 60.0               |
| Java 17      | 61.0               |
| Java 18      | 62.0               |
| Java 19      | 63.0               |
| Java 20      | 64.0               |
| Java 21      | 65.0               |
| Java 22      | 66.0               |
| Java 23      | 67.0               |
| Java 24      | 68.0               |

**说明**: Java版本通常以数字表示，如Java 1.0、Java 5、Java 8等。从Java 9开始，版本号采用了新的命名规则，例如Java 9、Java 10等。Class file版本是Java编译器编译Java源代码时生成的字节码文件（.class文件）的版本号。

### 特殊Java版本要求

特殊的模组或整合包可能有特殊的Java版本要求。如果在当前JVM上运行一个不被支持的Java版本，可能会抛出`java.lang.UnsupportedClassVersionError`错误，并指出支持的class file版本。

### java.exe和javaw.exe的区别

- `java.exe` 是Java命令行工具，用于在命令行界面中启动Java应用程序。
- `javaw.exe` 是Java的无窗口模式命令行工具，与`java.exe`功能相同，但它不会创建命令行窗口。

## 使用指南

- 使用本工具表确定您的Minecraft版本所需的Java版本。
- 如果遇到`UnsupportedClassVersionError`错误，请检查错误信息中指出的class file版本，并与上表对照以确定正确的Java版本。

---

**版权声明**: 本文档为开放资源，欢迎复制和分享，但请保留原始链接和版权信息。

**最后更新时间**: 2024-08-19