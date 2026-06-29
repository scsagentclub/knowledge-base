---
name: worldcup2026
github_url: https://github.com/rezarahiminia/worldcup2026
category: 好用工具
tags: [worldcup, api, sports, nodejs, express, mongodb, swagger, live-scores]
added_date: 2026-06-04
summary: 2026 年 FIFA 世界杯免费开源 REST API，提供实时比分、球队、分组、赛程和球场数据
---

## 项目简介

一个免费开源的 2026 年 FIFA 世界杯 REST API，覆盖完整赛事数据：48 支球队、12 个小组、104 场比赛、16 个主办球场。提供实时比分更新、JWT 认证、速率限制、缓存和 Swagger 交互式文档，适合开发世界杯相关的 App、Dashboard、Bot 和数据可视化应用。

## 主要特性

- 完整世界杯数据 API（球队、分组、赛程、球场、积分榜）
- 赛事期间实时比分与射手榜更新
- 多语言支持：英语 + 波斯语（Farsi）
- JWT 认证 + 请求速率限制 + 内存缓存
- Swagger/OpenAPI 3.0 交互式文档
- 提供 CSV/JSON 数据导入脚本，一键初始化 MongoDB

## 技术栈

- Node.js + Express.js
- MongoDB + Mongoose
- JWT 认证
- Swagger UI
- Helmet + express-rate-limit

## 适用场景

- 开发世界杯比分追踪 App、Dashboard
- 构建 Telegram / Discord 比赛通知 Bot
- 体育数据可视化与预测游戏
- 需要免费赛事数据的第三方项目

## 备注

- 公开 GET 接口无需 API Key 即可读取
- 写操作和需要认证的接口使用 JWT Token
- 关于进球时间是否区分加时/补时阶段，README 未明确说明字段格式，建议调用 `/get/game/${matchId}` 实测或查看源码
- 在线文档：https://worldcup26.ir/api-docs/
