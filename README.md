# DetecSee

DetecSee 是一个基于 NCNN 和 OpenCV 的 Android 目标检测应用，集成了 YOLOv8 模型，支持多种平台架构。

## 项目简介

DetecSee 旨在为 Android 设备提供高效的目标检测能力，利用 NCNN 推理引擎和 OpenCV 图像处理库，支持多种主流移动端硬件架构。项目内置 YOLOv8n 和 YOLOv8s 两种模型，适用于不同性能需求。

## 项目演示

![DetecSee 演示视频](https://github.com/user-attachments/assets/39ede45b-0a46-48c3-9b10-76995e78daa8)

## 项目结构

```
app/
├── build.gradle.kts                # App 构建配置
├── src/
│   ├── main/
│   │   ├── AndroidManifest.xml     # Android 清单文件
│   │   ├── assets/                 # 模型文件
│   │   │   ├── yolov8n.bin
│   │   │   ├── yolov8n.param
│   │   │   ├── yolov8s.bin
│   │   │   ├── yolov8s.param
│   │   ├── java/
│   │   │   └── sugar/me/detecsee/  # Java 源码
│   │   │       ├── MainActivity.java
│   │   │       ├── Yolov8Ncnn.java
│   │   ├── jni/                    # C++ 源码与第三方库
│   │   │   ├── ncnn-20250503-android-vulkan-shared/
│   │   │   ├── opencv-mobile-4.9.0-android/
│   │   │   ├── ndkcamera.cpp
│   │   │   ├── ndkcamera.h
│   │   │   ├── yolo.cpp
│   │   │   ├── yolo.h
│   │   │   ├── yolov8ncnn.cpp
│   │   ├── res/                    # 资源文件
│   │   │   ├── layout/
│   │   │   ├── drawable/
│   │   │   ├── mipmap-*/
│   │   │   ├── values/
│   │   │   ├── xml/
├── proguard-rules.pro              # 混淆规则
├── ...
```

## 主要功能

- 基于 NCNN 推理引擎，支持多平台（arm64-v8a, armeabi-v7a, x86, x86_64, riscv64）
- 集成 OpenCV 进行图像处理
- 支持 YOLOv8n、YOLOv8s 目标检测模型
- Android 原生相机采集与推理

## 快速开始

1. **环境准备**
- 安装 Android Studio
- 配置 NDK 和 CMake

2. **克隆项目**
   ```bash
   git clone https://github.com/zhsugar/DetecSee.git
   cd PixelNet
   ```

3. **用 Android Studio 打开项目**

4. **编译并运行**
   - 连接 Android 设备或启动模拟器
   - 点击运行按钮

## 依赖

- [ncnn](https://github.com/Tencent/ncnn)
- [OpenCV-Android](https://opencv.org/releases/)
- YOLOv8 模型（已包含在 assets/ 目录）

## 目录说明

- `app/src/main/java/`：Java 代码，包含主界面和 NCNN 调用逻辑
- `app/src/main/jni/`：C++ 代码，包含 NCNN、OpenCV 相关实现
- `app/src/main/assets/`：模型文件
- `app/src/main/res/`：资源文件（布局、图片等）

## 贡献指南

欢迎提交 Issue 和 Pull Request 来帮助改进 DetecSee！

