# static-file

静态资源仓库，用于集中存放可在 Web 项目中直接引用的字体文件与演示文稿模板。

## 目录结构

```
static-file/
├── fonts/                    # 字体资源
│   ├── noto-sans-sc/         # Noto Sans SC（思源黑体简体中文，woff2 子集）
│   ├── open-sans/            # Open Sans（TTF + demo）
│   ├── open-sans-woff2/      # Open Sans（woff2 格式）
│   └── ping-fang/            # PingFang SC（苹方，otf/ttf + demo + CSS）
├── pptx/                     # PPTX 模板与案例
└── README.md                 # 本文件
```

## 字体使用方式

本仓库中的字体均通过 CSS `@font-face` 进行了封装，可直接在网页中引用。

### Noto Sans SC

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/hepingmogul/static-file@main/fonts/noto-sans-sc/noto-sans-sc.css">
<style>
  body {
    font-family: 'Noto Sans SC', sans-serif;
  }
</style>
```

### PingFang SC

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/hepingmogul/static-file@main/fonts/ping-fang/pingfang.css">
<style>
  body {
    font-family: 'PingFang SC', sans-serif;
  }
</style>
```

### Open Sans

直接引用单个字体文件，或引用已封装好的 CSS：

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/hepingmogul/static-file@main/fonts/open-sans-woff2/open-sans-woff2.css">
<style>
  body {
    font-family: 'Open Sans', sans-serif;
  }
</style>
```

也可在本地项目中通过 `fonts/open-sans/demo.html` 查看 TTF 版本示例。

## 注意事项

1. **字体版权**：部分字体（如 PingFang SC）为商业字体，请确保在授权范围内使用；开源字体（Open Sans、Noto Sans SC）遵循对应开源协议。
2. **CDN 路径**：以上示例使用 jsDelivr CDN，路径中的用户名/仓库名请根据实际仓库地址调整。
3. **大文件**：`pptx/` 目录下文件较大，建议通过 Git LFS 或网盘分发，不宜直接通过 CDN 频繁下载。

## 贡献与维护

- 新增字体时，请同步提供对应的 CSS 封装与 demo 页面。
- 新增 PPTX 文件时，建议在文件名中体现主题或用途，方便检索。
