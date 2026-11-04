# 🤖 Project Rules & AI Agent Instructions (AGENTS.md)

## 1. 專案目的
本專案為一個靜態的「AI 工具與 Prompt 個人知識庫」。
旨在提供視覺統一、結構清晰且易於維護的 static HTML 筆記與教學頁面。

---

## 2. 專案目錄結構
/
├── index.html              # 網站首頁 (包含所有主題的卡片列表)
├── AGENTS.md               # 本開發規範文件
├── css/
│   └── style.css           # 全域主樣式表 (統一視覺規範)
└── pages/                  # 所有子頁面存放目錄
    └── claude-code.html    # 子頁面範例

---

## 3. 視覺風格與設計系統 (Design System & UI/UX)
修改或新建 HTML/CSS 時，必須使用全域 CSS 變數：
- 背景色：`--bg-primary: #0f172a` (深藍暗色系)
- 卡片背景：`--bg-card: #1e293b`
- 文字主色：`--text-main: #f8fafc`
- 文字次色：`--text-muted: #94a3b8`
- 強調點綴色：`--accent: #38bdf8` (亮藍色)
- 版面配置：最大寬度 `1000px` 自動置中；手機端自動切換為單欄模式。

---

## 4. 新增內容標準 SOP
當使用者要求新增頁面時，AI Agent 必須執行以下兩步：
1. **建立頁面**：在 `pages/` 下建立檔名為 kebab-case 的 HTML 檔（例如 `pages/midjourney-tips.html`），繼承 `css/style.css` 並包含頂部導覽列、標籤與內容區塊。
2. **自動更新索引**：同步修改 `index.html`，在卡片牆頂部新增對應的連結卡片。

---

## 5. AI 執行原則
1. 零外部依賴：使用原生 HTML5 + CSS3，確保 GitHub Pages 免編譯部署。
2. 樣式嚴格一致：所有子頁面一律引用 `../css/style.css`。