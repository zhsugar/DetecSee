# DetecSee - 安卓目标检测识别应用

DetecSee 是一个基于安卓平台的目标检测识别应用，能够实时识别摄像头画面中的物体并提供准确的检测结果。

## 功能特性

- 📱 **实时目标检测**：利用设备摄像头进行实时物体识别
- 🎯 **高精度识别**：基于深度学习模型，提供准确的检测结果
- ⚡ **快速响应**：优化的推理引擎，确保流畅的用户体验
- 🎨 **直观界面**：简洁易用的用户界面设计
- 📊 **结果展示**：可视化检测框和置信度分数

## 演示视频

![DetecSee 演示视频](https://github.com/user-attachments/assets/39ede45b-0a46-48c3-9b10-76995e78daa8)

## 技术栈

- **开发语言**：Kotlin/Java
- **机器学习框架**：TensorFlow Lite / ML Kit
- **目标检测模型**：YOLO / MobileNet SSD
- **UI框架**：Android Jetpack Compose / XML Layout
- **最低支持版本**：Android 7.0 (API 24)

## 安装指南

### 环境要求
- Android Studio Arctic Fox 或更高版本
- Android SDK 24 或更高版本
- 至少 2GB RAM 的设备

### 构建步骤

1. **克隆项目**
   ```bash
   git clone [项目仓库地址]
   cd DetecSee
   ```

2. **打开项目**
   - 在 Android Studio 中打开项目
   - 等待 Gradle 同步完成

3. **配置模型**
   - 将训练好的模型文件放入 `app/src/main/assets/` 目录
   - 确保模型文件名与代码中引用的一致

4. **构建并运行**
   - 连接安卓设备或启动模拟器
   - 点击 "Run" 按钮构建并安装应用

## 使用说明

1. **启动应用**：点击应用图标启动 DetecSee
2. **权限授权**：授予相机权限以使用目标检测功能
3. **开始检测**：将摄像头对准想要识别的物体
4. **查看结果**：应用会实时显示检测到的物体和置信度

## 项目结构

```
DetecSee/
├── app/
│   ├── src/main/
│   │   ├── java/com/detect/see/      # 主要代码
│   │   ├── res/                      # 资源文件
│   │   └── assets/                   # 模型文件
│   └── build.gradle.kts             # 应用级构建配置
├── build.gradle.kts                   # 项目级构建配置
├── gradle.properties                 # Gradle 配置
└── settings.gradle.kts               # 项目设置
```

## 常见问题

**Q: 应用启动后立即崩溃**
A: 请检查是否正确放置了模型文件，并确认设备支持 Camera2 API。

**Q: 检测精度不够高**
A: 尝试在光线充足的环境下使用，或考虑使用更高精度的模型。

**Q: 检测速度较慢**
A: 在设置中启用 GPU 加速，或降低输入图像分辨率。

## 贡献指南

欢迎提交 Issue 和 Pull Request 来帮助改进 DetecSee！
