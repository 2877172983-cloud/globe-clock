# 深空制图仪 · 手势三维地球

一种用手掌操作的三维点阵地球。浏览器打开即用，无需安装。

🔗 **在线体验：https://2877172983-cloud.github.io/globe-clock/**

> 微信内无法使用摄像头，请点右上角 ··· 选择「在浏览器打开」。

## 功能

- 手掌移动 → 转动地球
- 五指开合 → 缩放
- 拇指食指捏合 → 抓住地球拖动
- 点击城市 → 飞行定位到该城市
- 鼠标可用：拖拽旋转、滚轮缩放、点击定位

## 技术栈

- p5.js（canvas 2D）
- MediaPipe Hands（浏览器端手部追踪）
- 纯前端，无后端、无构建工具

## 项目来源

本项目基于 [Wencle-Sun/globe](https://github.com/Wencle-Sun/globe)
（MIT License，Copyright © Wencle Sun）扩展。

### 我新增的部分

1. **城市标签系统**：三级分级（一级 8 个 / 二级 26 个 / 三级 45 个），
   文字描边（strokeText + fillText 双层渲染），矩形碰撞避让，缩放联动淡入
2. **行星与月球**：新增土星（带环）、木星（条纹 + 大红斑）、火星（极冠）；
   月球补充环形山与第谷辐射纹
3. **性能优化**：把每帧 300+ 次 `createRadialGradient` 改为预渲染 sprite，
   帧时间从 55.5 ms 降到 16.7 ms

### 我未改动的部分

点阵地球、手势识别核心逻辑、城市与航线数据、观察者模式，均为原作者实现。

## 许可

MIT License，见 [LICENSE](./LICENSE)。
第三方库与素材的许可见原作者仓库的 `THIRD_PARTY_NOTICES.md`。
