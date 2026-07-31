# Transit Go · 出行导航

一个移动端优先的公交/地铁路线规划网站，帮你在陌生城市快速找到怎么去目的地。

## 在线访问

**https://guyu476.github.io/transit-go/**

## 功能

- 🗺️ 地图浏览（默认高德，可切换 OSM/CartoDB）
- 📍 GPS 自动定位
- 🔍 地点搜索（高德 POI 提示，输入即出建议）
- 🚇 公交/地铁换乘路线规划（多方案对比）
- 🚶 步行 / 驾车路线
- 🔀 一键交换起点终点
- ⭐ 路线收藏（保存在浏览器本地，反复使用）
- 🚉 公交/地铁线路分段彩色显示 + 上/下车站点标记
- 🔄 自动接驳（目的地公交地铁到不了时自动找最近站点）
- ⚙️ 可收起设置面板（高德 Key 管理 + 地图风格切换）

## 技术栈

| 层 | 技术 | 链接 |
|---|---|---|
| 地图引擎 | Leaflet.js 1.9.4 | https://leafletjs.com |
| 地图瓦片 | 高德 / OpenStreetMap / CartoDB | 高德 tile: `webrd0{s}.is.autonavi.com` |
| 地点搜索 | 高德 Input Tips API | https://restapi.amap.com/v3/assistant/inputtips |
| 公交换乘 | 高德公交路线 API | https://restapi.amap.com/v3/direction/transit/integrated |
| 步行导航 | 高德步行路线 API | https://restapi.amap.com/v3/direction/walking |
| 驾车导航 | 高德驾车路线 API | https://restapi.amap.com/v3/direction/driving |
| 周边站点 | 高德周边搜索 API | https://restapi.amap.com/v3/place/around |
| 部署 | GitHub Pages | https://pages.github.com |

## 免费额度

高德 Web服务 API 免费额度（个人开发者）：

- 地点搜索：1000 次/天
- 路线规划：1000 次/天
- 日常个人使用完全够

## 如何获取高德 Key

1. 打开 https://lbs.amap.com/
2. 注册/登录 → 创建应用
3. 添加 Key，**服务平台选「Web服务」**
4. 复制 Key，打开网站右侧 ⚙️ 设置面板填入保存

## 本地预览

```bash
cd transit-go
python -m http.server 8080 -d docs
# 打开 http://localhost:8080
```

## 项目结构

```
transit-go/
├── docs/
│   └── index.html    # 全部代码（单文件，无需构建）
├── .gitignore
└── README.md
```

## 数据来源

- 地图底图：高德地图（无需Key可浏览）
- 地点数据：高德开放平台
- 路线数据：高德开放平台
