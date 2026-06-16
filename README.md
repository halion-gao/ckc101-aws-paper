# labor-ai-web-agent 專題里程碑簡報系統

本專案為 `labor-ai-web-agent` 的 AWS/GCP 專題里程碑簡報系統。採用純網頁 HTML5 / CSS3 / JavaScript 開發，具備高階諮詢暗色風格設計與現代化互動式放映功能，旨在清晰呈現中小微企業數位轉型與智慧勞動法遵 AI 的實踐歷程。

## 🌐 線上展示與預覽
簡報已發布於 GitHub Pages，您可以直接透過以下網址進行播放與觀看：
👉 **[https://halion-gao.github.io/ckc101-aws-paper/](https://halion-gao.github.io/ckc101-aws-paper/)**

---

## ✨ 系統核心亮點

1. **單頁放映引擎 (Slideshow Engine)**
   * 內建單頁播放邏輯，摒棄傳統長網頁滾動，提供如 PowerPoint / Keynote 般的投影片放映體驗。
   * **快捷鍵操作**：支援 `←` (上張)、`→` / `Space` (下張)、`F` (切換全螢幕)、`Esc` (切換簡報網格總覽)。
   * **行動裝置手勢**：支援在手機與平板上透過左右滑動 (Swipe) 切換投影片。
2. **投影片總覽模式 (Grid Overview)**
   * 點選懸浮控制列上的總覽圖示（或按 `Esc`），即可開啟全螢幕格狀縮圖面板，點選即可快速跳轉至指定投影片。
3. **自適應視窗縮放 (Responsive Auto-Scaling)**
   * 內建視窗重置監聽器，會根據當前瀏覽器視窗大小，自動利用 CSS `transform: scale()` 對簡報容器進行無損比例縮小，確保在小螢幕筆電或大螢幕投影機上都能維持完美比例且「無滾動條」。
4. **數據圖表優化**
   * 對 Token 成本對比、審查時間對比等長條圖進行排版優化。數值文字與著色比例條分離，保證極窄比例條（如 8%）在任何裝置上均不會產生文字折行或壓住下方卡片的問題。
5. **列印與匯出最佳化 (@media print)**
   * 完美支援瀏覽器原生 PDF 列印功能，保留所有主題背景、霓虹光暈與 Icon 設計。

---

## 💻 本地端預覽步驟

若您想在本地端執行或修改專案，請參考以下步驟：

1. 克隆此儲存庫：
   ```bash
   git clone https://github.com/halion-gao/ckc101-aws-paper.git
   ```
2. 進入專案目錄，並使用 Python 啟動輕量 Web 伺服器：
   ```bash
   cd ckc101-aws-paper
   python3 -m http.server 3000
   ```
3. 在瀏覽器中開啟：
   👉 **[http://localhost:3000](http://localhost:3000)**

---

## 📥 如何匯出成 PDF 簡報檔案

本專案支援將簡報以 1:1 高保真度匯出為 PDF 檔案：

1. 在瀏覽器中打開簡報頁面。
2. 按下列印快速鍵：
   * **Mac**: `Cmd + P`
   * **Windows/Linux**: `Ctrl + P`
3. 在瀏覽器的列印設定中進行如下調整：
   * **目的地 (Destination)**：選擇 **「另存為 PDF」(Save as PDF)**。
   * **方向 (Layout)**：選擇 **「橫向」(Landscape)**。
   * **邊界 (Margins)**：選擇 **「無」(None)**。
   * **選項 (Options)**：勾選 **「背景圖形」(Background graphics)**（此步驟非常重要，能確保深色背景與彩色比例條正常匯出）。
4. 點選 **「儲存」(Save)** 即可完成簡報匯出！

---

## 📁 專案檔案結構說明
```text
├── .gitignore              # Git 過濾配置
├── .vscode/
│   └── 1.html              # 備份簡報源代碼
├── assets/                 # 視覺素材資料夾
│   ├── handbook_user.png   # 勞動部 114 年工時手冊真實封面
│   ├── voice_wave.png      # Slide 9 語音多模態視覺配圖
│   └── ocr_scan.png        # Slide 9 班表拍照識別視覺配圖
├── README.md               # 專案說明文件（本檔案）
├── index.html              # 簡報系統主入口檔案 (GitHub Pages 預設服務頁面)
└── slides.html             # 簡報系統備份入口檔案
```

---
*本簡報專案由 Halion Gao 配合 AI 代理人協同設計優化。*