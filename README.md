# 天地通设备部署规划系统

一个基于 Three.js 的3D设备部署可视化系统，支持"1托18"规则的蜂窝状六边形覆盖模型。

## 功能特点

- 📍 **六边形网格布局**：采用 flat-top 坐标系，实现边对边紧密贴合
- 🎯 **1托18部署规则**：每组包含1台中心设备+18台从设备，共19台
- 📊 **实时统计**：显示覆盖面积、设备总数、总造价等关键参数
- 🎨 **精美3D模型**：包含设备模型、信号波动画、尺寸标注
- 🖱️ **交互功能**：支持旋转、缩放、平移、拖拽组中心

## 快速开始

### 本地运行

```bash
# 使用任意静态服务器启动
python -m http.server 8000
# 或
npx serve .
```

然后访问 http://localhost:8000/tianditong_3d_deploy.html

### GitHub Pages 部署

1. **创建 GitHub 仓库**
   - 在 GitHub 上创建一个新仓库（建议命名：tianditong-deploy）

2. **上传文件**
   ```bash
   # 初始化仓库
   git init
   git add .
   git commit -m "Initial commit"
   
   # 添加远程仓库
   git remote add origin https://github.com/yiming-zihan/tianditong-deploy.git
   git push -u origin main
   ```

3. **启用 GitHub Pages**
   - 进入仓库 Settings → Pages
   - Source 选择 `main` 分支，点击 Save
   - 访问地址：https://yiming-zihan.github.io/tianditong-deploy/tianditong_3d_deploy.html

## 技术栈

- Three.js - 3D图形渲染
- OrbitControls - 3D视角控制
- 原生 JavaScript / HTML5 Canvas

## 文件结构

```
.
├── tianditong_3d_deploy.html  # 主页面
├── lib/
│   ├── three.min.js           # Three.js 核心库
│   └── OrbitControls.js       # 视角控制
└── README.md                  # 项目说明
```

## 使用说明

- **左键拖动**：旋转视角
- **滚轮**：缩放
- **右键拖动**：平移
- **拖拽组中心设备**：移动布局
- **顶部按钮**：切换部署模式（1托6/1托18/3组/6组/9组/12组/20组）
