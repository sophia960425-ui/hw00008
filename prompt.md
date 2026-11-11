# 大二影展專題《話外之協》—— AI 協作 Prompt 說明與專案發展紀錄

本文件紀錄在開發逢甲大學行銷系大二影展專題《話外之協》網站專案時，與 AI 協作時所使用的 Prompt（提示詞）架構、迭代過程與開發策略。

---

## 📌 一、 專案基本資訊
* **專案名稱**：大二影展專題《話外之協：走出話裡的想像，看見話外的東協》
* **開發作者**：翁湘羚（逢甲大學行銷系）
* **專案目的**：透過網頁呈現東協廣場之文化體驗、行銷企劃（STP/SWOT）、故事分鏡與影展參展影片成果。
* **技術堆疊**：HTML5, CSS3 (CSS Grid, Flexbox, Custom Properties), JavaScript, Vercel / InfinityFree 部署。

---

## 💡 二、 Prompt 提示詞設計策略

為了讓 AI 能精確生成符合行銷系影展專案要求的程式碼與內容，提示詞採取了以下結構化設計：

1. **角色設定 (Persona)**：指定 AI 擔任資深前端工程師與行銷視覺設計師。
2. **語意結構規範**：要求採用標準 HTML5 語意標籤 (`<header>`, `<nav>`, `<main>`, `<aside>`, `<section>`, `<footer>`, `<details>`)。
3. **視覺美學規範**：指定「粉咖暖色系」（#b56576 主色、#faedeb 襯色、#4a3b32 深可可字體），營造溫馨且具文化質感的視覺氛圍。
4. **功能性要求**：
   * 包含完整 SEO Meta 標籤與 Open Graph 社交分享標籤。
   * 具備雙頁籤分頁（Tab Switch）切換機制。
   * 使用 CSS Grid 與 Flexbox 實現響應式排版 (RWD)。
   * 將 CSS 切割為 `layout.css`, `navigation.css`, `components.css` 分置於 `css/` 資料夾中。

---

## 📝 三、 核心 Prompt 紀錄 (Prompt Log)

### 1. 結構與行銷企劃內容生成 Prompt
> **Prompt:**
> 「請協助我為大二影展專題《話外之協》設計一個具備 SEO 標籤、雙欄排版、頂部導覽列與側邊欄的網頁。內容需包含東協廣場的背景介紹、競品分析表格 (INDEX 南洋百貨 vs RJ Supermart)、SWOT 與 STP 行銷策略、參展影片 YouTube 嵌入、故事腳本分鏡 (Storyboard) 以及團隊 8 人核心分工。」

### 2. 視覺樣式與 RWD 響應式排版 Prompt
> **Prompt:**
> 「請使用粉咖色系（暖色調 #b56576）為《話外之協》專案撰寫 CSS 樣式。需包含 CSS Grid 網格系統卡片、Hero Banner 區塊、精美表格與手機版 RWD 響應式斷點 (Media Query)。請將 CSS 切割為 layout.css（版面）、navigation.css（導覽列與側邊欄）與 components.css（元件與卡片）三份檔案。」

### 3. 分頁切換功能與部署調校 Prompt
> **Prompt:**
> 「請在 HTML 中加入 JavaScript 分頁切換機制，將內容分為『分頁 1：專題企劃與策略』與『分頁 2：影片與分鏡團隊』。同時確保所有圖片與樣式路徑正確對應 `css/` 與 `images/` 資料夾，以順利部署至 GitHub / Vercel 與 InfinityFree。」

---

## 📂 四、 GitHub 專案檔案結構

```text
hw0008/
├── index.html              # 主頁面 (包含 SEO、語意標籤與 JavaScript 分頁)
├── prompt-guide.md         # 本 Prompt 說明文件
├── css/
│   ├── layout.css          # 全域變數、版面配置與 RWD 斷點
│   ├── navigation.css      # 導覽列與側邊欄選單樣式
│   └── components.css      # 卡片、表格、Hero Banner 與粉咖元件樣式
└── images/
    └── poster-cover.jpg    # 影展封面與視覺圖片
