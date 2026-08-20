# Best-Browser

一个基于 [igv.js](https://github.com/igvteam/igv.js) 的在线基因组浏览器，支持小鼠 mm10 和人类 hg38 两个参考基因组。整个工具就是一个独立的 HTML 文件，不需要安装、不需要服务器，双击（或用浏览器打开）就能用。

在线体验：https://hengbingao.github.io/Best_browser/browser/genome_browser_cn.html

## 目录结构

```
Best_browser/
├── README.md
└── browser/
    ├── genome_browser_cn.html   # 中文版
    └── genome_browser_en.html   # 英文版
```

两个文件功能完全一样，只是界面语言不同，用哪个都可以，各自独立、不需要额外依赖。

## 功能

- 内置 mm10（小鼠）/ hg38（人类）参考基因组，页面顶部下拉切换
- 内置 RefSeq 基因注释轨道，同一个基因只保留最长的转录本，不会看到一堆重复条目
- 支持基因名或坐标（如 `chr1:3,000,000-3,700,000`）搜索跳转
- 支持加载本地文件 / 整个文件夹里的轨道（bigWig、bed、vcf 等），也支持粘贴 URL 直接加载在线轨道
- 轨道可以批量设置高度、颜色，可以做 Group scale / Auto scale
- 支持把当前的基因组、坐标、所有轨道配置保存成一个 Session（json），下次选中对应文件夹即可一键还原（只有一个 Session 文件时自动加载，多个的话会弹窗让你选）

## 使用方法

1. 打开 `browser/genome_browser_cn.html`（或英文版 `genome_browser_en.html`）
2. 顶部选择参考基因组（mm10 / hg38）
3. 在“跳转 / 搜索”里输入基因名或坐标，点 Go
4. 需要加载自己的数据：点“选择本地文件”或“选择文件夹加载”，也可以粘贴轨道的 URL
5. 调整好轨道顺序、颜色、高度后，可以点“保存 Session”导出配置，下次用“加载 Session”一键还原
