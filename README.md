# 手势控制 3D 粒子系统

用摄像头手势控制的 Three.js 粒子作品。基于 MediaPipe Hands 做手部关键点识别，
Three.js 渲染 15000 个粒子。

## 玩法

- **捏合拇指与食指** → 粒子凝聚收缩
- **张开手掌** → 粒子扩散 / 爆炸
- 右上角面板可切换 6 种形态：爱心 / 花朵 / 土星 / 佛像（拟） / 烟花 / 球体
- 取色器可改粒子颜色
- **没有摄像头也能玩**：拖动「粒子聚散」滑块即可控制

## 运行要求

- 必须是 **HTTPS 或 localhost** 环境（浏览器规定：非安全上下文禁止调用摄像头）
- 首次打开会请求摄像头权限，允许即可
- 需要联网（Three.js r128 与 MediaPipe 从 CDN 加载）
- 建议用 Chrome / Edge

## 技术栈

- Three.js r128（Points + AdditiveBlending 粒子）
- MediaPipe Hands（21 个手部关键点，取拇指尖 #4 与食指尖 #8 的距离映射到粒子缩放）

## 说明

单文件 HTML，无构建步骤。修改 `index.html` 提交后 GitHub Pages 会自动重新构建。
