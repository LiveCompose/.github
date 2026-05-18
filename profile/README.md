# 构妙 LiveCompose

**基于强化学习的 AI 端侧智能构图辅助系统**

[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Models%20%26%20Datasets-yellow)](https://huggingface.co/LiveCompose)
[![App Store](https://img.shields.io/badge/App_Store-构妙_LiveCapture-blue)](https://apps.apple.com/cn/app/%E6%9E%84%E5%A6%99/id6754213088)

---

构妙 LiveCompose 致力于让每一位普通用户都能轻松拍出专业级构图照片。不同于传统相机的静态九宫格辅助线，我们通过 AI 实时分析取景画面，结合设备陀螺仪实现物理级追踪引导，主动"告诉"用户如何移动手机以获得最佳构图，并在对齐完美构图时自动拍摄。

## Projects

| 项目 | 说明 |
|------|------|
| [LiveCompose](https://github.com/LiveCompose/LiveCompose) | RL 模型训练、知识蒸馏、CoreML 部署 |
| [LiveCapture](https://github.com/LiveCompose/LiveCapture) | iOS APP 源码 | 

## 技术栈

- **模型架构**: ResNet50 Backbone + Actor-Critic (PPO)
- **美学评分**: NIMA / GAIC 双评分器驱动奖励信号
- **数据构建**: BLIP + Stable Diffusion Inpaint 双模型工作流
- **端侧部署**: 知识蒸馏 (MobileNetV3-Small) → CoreML → iOS
- **应用框架**: SwiftUI + AVFoundation + CoreMotion + CoreML

## 关键特性

- **实时动态引导**：AI 分析画面，可视化移动指引
- **传感器融合追踪**：陀螺仪 + 磁性吸附，物理级流畅追踪
- **美学评分驱动**：NIMA/GAIC 模型确保构图专业性
- **闭环体验**：检测 → 追踪 → 引导 → 拍摄，全流程自动化
- **端侧高效推理**：蒸馏后的轻量模型在 iOS 设备上实时运行

## 模型与数据集

预训练模型权重、训练数据集及 Demo 托管在 Hugging Face：

[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-LiveCompose-yellow)](https://huggingface.co/LiveCompose)

## App

[iOS App: 构妙 LiveCapture](https://apps.apple.com/cn/app/%E6%9E%84%E5%A6%99/id6754213088) — 已上架 App Store

---

*构妙 LiveCompose — 让每一次快门，都定格最美的瞬间.*
