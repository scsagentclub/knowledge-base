---
name: claude-desktop-buddy
github_url: https://github.com/anthropics/claude-desktop-buddy
category: 硬件开发
tags: [esp32, ble, claude, hardware, maker, desktop-pet, m5stickc]
added_date: 2026-06-04
summary: Claude 桌面端的硬件伴侣，通过 BLE 连接 ESP32 设备，实现桌面宠物、权限审批和消息互动
---

## 项目简介

Anthropic 官方推出的 Claude 桌面端硬件伴侣项目。通过蓝牙低功耗（BLE）将 Claude macOS/Windows 与 ESP32  maker 设备连接，让开发者和硬件爱好者可以构建能显示权限提示、最近消息和互动状态的物理设备。

官方示例是一个基于 M5StickC Plus 的桌面宠物：没动静时睡觉，Claude 开始工作时醒来，有权限待审批时会焦急闪烁，还可以直接在设备上 approve 或 deny。

## 主要特性

- BLE 无线连接 Claude 桌面端（Nordic UART Service）
- 设备端直接 approve/deny 权限请求
- 18 种内置 ASCII 宠物，每种 7 种动画状态
- 支持自定义 GIF 角色（拖拽文件夹即可推送）
- 能量/升级系统（每 50K tokens 升一级）
- 自动熄屏、摇晃互动、面朝下休眠等物理交互

## 技术栈

- ESP32 + Arduino 框架
- PlatformIO 构建系统
- M5StickC Plus（屏幕 + IMU + 按键）
- BLE Nordic UART Service
- C++ 固件 + JSON 状态协议

## 适用场景

- 硬件爱好者/maker 想做 Claude 的实体桌面宠物
- 想从物理设备端直接审批 Claude 权限的开发者
- 想研究 Claude 桌面端 BLE API 的开发者（需开启 Developer Mode）

## 备注

- BLE API 仅在 Claude 桌面端开启 Developer Mode 时可用
- 该功能面向 maker 和开发者，非官方正式支持的产品特性
- 自定义 GIF 角色需控制在 1.8MB 以内
