# Best-Browser

An online genome browser built on [igv.js](https://github.com/igvteam/igv.js), supporting the mouse (mm10) and human (hg38) reference genomes. The whole tool is a single self-contained HTML file — no install, no server. Just open it in a browser.

Live demo: https://hengbingao.github.io/Best_browser/browser/genome_browser_cn.html

## Repository structure

```
Best_browser/
├── README.md
└── browser/
    ├── genome_browser_cn.html   # Chinese UI
    └── genome_browser_en.html   # English UI
```

Both files have identical functionality — only the UI language differs. Either one works standalone with no extra dependencies.

## Features

- Built-in mm10 (mouse) / hg38 (human) reference genomes, switchable from a dropdown at the top of the page
- Built-in RefSeq gene annotation track that keeps only the longest transcript per gene, so you won't see a pile of duplicate entries
- Search and jump by gene name or coordinates (e.g. `chr1:3,000,000-3,700,000`)
- Load local files or an entire local folder of tracks (bigWig, bed, vcf, etc.), or paste a URL to load a track directly from the web
- Batch-set track height and color, plus Group scale / Auto scale
- Save the current genome, locus, and all track settings as a Session (JSON); next time, just pick that folder to restore it in one click (auto-restores if there's exactly one Session file, or lets you pick when there are several)

## Usage

1. Open `browser/genome_browser_en.html` (or the Chinese version `genome_browser_cn.html`)
2. Choose a reference genome (mm10 / hg38) at the top
3. Type a gene name or coordinates into the search box and click Go
4. To load your own data: click "Choose local file" or "Choose folder to load", or paste a track URL
5. Once tracks are arranged with the order, color, and height you want, click "Save Session" to export the config, and "Load Session" next time to restore it in one click
