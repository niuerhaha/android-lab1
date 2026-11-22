# 实验一：创建空项目

Android 课程实验一 —— 用 Android Studio 新建一个空项目并运行，熟悉工程结构与构建流程。

## 环境

| 项目 | 版本 |
|---|---|
| Android Gradle Plugin | 9.3.3 |
| Gradle | 9.5.0 |
| 语言 | Kotlin 2.2.10（Compose） |
| compileSdk / targetSdk | 37 |
| minSdk | 24 |

## 工程结构

```
实验一/
├── build.gradle                 顶层构建脚本（AGP 插件版本）
├── settings.gradle              仓库源与模块声明
├── gradle.properties            Gradle 全局参数
├── gradle/                      Gradle 版本与 JDK 工具链配置
└── app/
    ├── build.gradle             app 模块配置与依赖
    └── src/main/
        ├── AndroidManifest.xml  应用清单（注册 MainActivity 为启动页）
        ├── java/com/example/lab1/MainActivity.kt
        └── res/
            ├── drawable/ic_launcher.xml
            └── values/{strings,themes}.xml
```

## 内容说明

- 采用 Android Studio 默认的 **Empty Activity** 模板，只保留一个 `MainActivity`。
- 界面用 Compose 写了一个 `Greeting` 组件，启动后显示 `Hello Android!`。
- 没有任何业务逻辑，目的是验证 SDK、Gradle、模拟器链路是通的。

## 运行

用 Android Studio 打开本目录，等待 Gradle 同步完成后点 Run；或命令行：

```bash
gradle assembleDebug
```

生成的安装包位于 `app/build/outputs/apk/debug/app-debug.apk`。
