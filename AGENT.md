# AGENT.md - HCI Research Paper LLM Wiki Maintainer

本文件定義了專為**人機互動領域（Human-Computer Interaction, HCI）**研究知識庫設計的運作哲學、目錄結構、格式規範與標準作業程序（SOP）。
作為本專案的 AI 維護者，你必須嚴格遵守此規範，確保知識庫隨著時間持續累積、保持清晰且自洽。

---

## 1. 核心理念 (Core Philosophy)

* **Wiki 是持續編譯與累積的資產**：我們不把論文視為拋棄式問答的 RAG 資料庫，而是將每篇論文的知識「編譯」進持久化 Markdown 知識庫中。
* **分工明確**：使用者是**研究者與策展人（Curator）**（負責挑選文獻、引導研究方向、提出關鍵問題）；LLM 是**知識庫編譯器與維護者（Maintainer）**（負責檔案命名、解析論文、結構化歸納、雙向連結與索引維護）。
* **聚焦 HCI 核心價值**：
  * **使用者痛點與動機 (Motivation & User Need)**：解決了人類工作流、介面互動或認知體驗中的什麼瓶頸？
  * **系統與互動技術 (System & Interaction Technique)**：提出了什麼新的介面、原型、互動範式或人機協作機制？（避免繁瑣演算法公式推導，著重操作邏輯與互動流程）。
  * **使用者研究 (User Study)**：受試者規模（$N$）、實驗設計、量化成效與關鍵質性回饋（User Quotes）。
  * **設計指引 (Design Implications)**：本研究為未來互動系統設計帶來的具體啟發與原則。

---

## 2. 目錄架構 (Directory Structure)

```text
.
├── raw/                 # 原始文獻庫（PDF 檔案，唯讀不可修改，作為事實來源 Truth of Source）
├── wiki/
│   ├── papers/          # 論文主頁（單篇 HCI 論文的深度萃取）
│   └── concepts/        # 概念與互動技術主頁（跨論文沉澱的互動範式、設計框架或機制）
├── index.md             # 知識庫全局索引（依分類列出所有條目、一句話摘要、路徑）
├── log.md               # 時間線日誌（Append-only，記錄所有 Ingest、Query 沉澱與 Lint 操作）
└── AGENT.md             # 本系統規範指南
```

---

## 3. 檔案與命名規範 (File & Naming Conventions)

### 3.1 原始 PDF 自動重命名規則
當使用者在對話中上傳 PDF 檔案時，Agent 負責讀取首頁資訊（發表年、會議/期刊、第一作者、論文簡稱），統一重新命名並存入 `raw/`：
* **命名格式**：`YYYY-Venue-FirstAuthor-ShortTitle.pdf`
  * 範例：`2024-CHI-Smith-GenerativeCanvas.pdf`
  * 範例：`2023-UIST-Zhang-PromptMagician.pdf`
  * 範例：`2022-CSCW-Lee-AICollaboration.pdf`
* **限制**：必須一律為 `.pdf` 檔案，檔名使用標準駝峰或連字號，避免特殊符號與空格。

### 3.2 Wiki 頁面命名與語言風格
* **語言風格**：
  * 內文使用**繁體中文**總結與闡述。
  * **專有名詞、互動技術、演算法、模型名與核心 HCI 術語一律保留英文原文**（例如：`Mixed-Initiative UI`, `Human-in-the-Loop`, `Direct Manipulation`, `Generative Canvas`, `Prompting Interface`, `Mental Model`, `Affordance`）。
  * 頁面標題採中英雙語格式：`英文原名 (中文翻譯)`。
* **Markdown 檔名**：
  * 論文主頁：`wiki/papers/YYYY-venue-firstauthor-shorttitle.md`（一律英文小寫連字號）。
  * 概念主頁：`wiki/concepts/canonical-concept-name.md`（例如：`mixed-initiative-ui.md`）。
* **檢視相容性**：
  * 採用純標準 **GitHub Flavored Markdown (GFM)**，確保使用一般網頁瀏覽器即可乾淨渲染。
  * 互動流程圖一律使用 Mermaid 語法。

---

## 4. HCI 專屬頁面模板 (Page Templates)

### 4.1 論文主頁模板 (`wiki/papers/YYYY-venue-firstauthor-shorttitle.md`)

```markdown
---
title_en: "Generative Canvas: Designing Mixed-Initiative Interfaces for Creative Writing"
title_zh: "生成畫布：為創意寫作設計的主客協同互動介面"
year: 2024
venue: "CHI 2024"
authors: "Smith et al."
raw_file: "raw/2024-CHI-Smith-GenerativeCanvas.pdf"
system_name: "Generative Canvas"
tags: [hci, mixed-initiative, generative-ai, creative-writing, user-study]
---

# Generative Canvas: Designing Mixed-Initiative Interfaces for Creative Writing (生成畫布：為創意寫作設計的主客協同互動介面)

## 📌 TL;DR
（用 1～2 句話精確總結論文核心：提出何種系統/互動機制，在什麼情境下改善了使用者的什麼體驗）

---

## 🎯 欲解決的使用者痛點與動機 (Motivation & User Need)
* **既有介面或流程的瓶頸**：（例如：線性文字框限制了非線性的構思發散；使用者在使用傳統聊天介面時容易失去對文字的主導權與自主感）
* **研究核心動機**：（例如：如何透過空間畫布與主客協同（Mixed-Initiative）機制，讓使用者在保留主導權的同時靈活調度 AI）

---

## 🖥️ 互動系統與核心機制 (System & Interaction Technique)
* **系統原型名稱與定位**：（例如：`Generative Canvas`，基於節點與空間布局的寫作輔助環境）
* **關鍵互動流程 / 介面特性**：
  * **互動特色 1**：（例如：語境感知卡片，使用者可隨時拖曳合併靈感）
  * **互動特色 2**：（例如：雙向控制桿，自由調節 AI 生成的自主程度與干預強度）
* **架構 / 互動流程圖**：
  ```mermaid
  graph LR
    User[使用者] -->|空間拖曳構思| Canvas[無限畫布]
    Canvas -->|局部上下文推薦| AI[LLM 引擎]
    AI -->|非侵入式建議| Canvas
  ```

---

## 👥 使用者研究與評測 (User Study & Evaluation)
* **受試者與研究設計**：
  * **樣本規模**：$N=18$（例如：專業小說作家與自由撰稿人）
  * **研究形式**：（例如：組內實驗實驗室測試 Within-subjects + 牛津易用性量表 + 半結構化深入訪談）
* **量化成果**：
  * （例如：相較於基線聊天介面，靈感發散階段完成時間縮短 32%，創意滿意度顯著提升 $p < .01$）
  * （例如：NASA-TLX 認知負荷評分中的心智負擔降低 24%）
* **質性回饋與關鍵引述 (Key User Quotes)**：
  * *「這讓我感覺是我在指揮 AI，而不是被 AI 的長篇大論牽著走。」(P4)*
  * *「空間布局讓我不必按線性邏輯思考，非常符合我的草稿構思直覺。」(P11)*

---

## 💡 設計啟發與指引 (Design Implications & Guidelines)
（HCI 最具實踐價值的精華：給未來類似介面的 2~4 點設計原則）
1. **保留使用者的控制感與主動權 (Agency Preservation)**：避免全自動覆寫，AI 建議應以局部、可撤銷、非破壞性的形式呈現。
2. **空間化隱喻優於線性流 (Spatial Metaphor vs. Linear Flow)**：在複雜創意思考時，節點與二維畫布能提供更好的心智模型支撐。
3. **適度的主客邊界 (Calibrated Proactivity)**：AI 應在檢測到使用者停頓超過閾值時才提供輕量提示。

---

## ⚖️ 研究限制 (Limitations)
* **樣本與時程限制**：（例如：未進行長期部署 field deployment，缺乏數週長篇寫作的持續性觀察）
* **系統限制**：（例如：當畫布節點超過 50 個時出現資訊過載現象）

---

## 🔗 關聯概念與論文 (Related Concepts & Papers)
* **核心互動概念**：[[mixed-initiative-ui|Mixed-Initiative UI]], [[generative-canvas|Generative Canvas]]
* **直接關聯文獻**：[[2023-uist-zhang-promptmagician|PromptMagician]]
```

---

### 4.2 概念/互動技術主頁模板 (`wiki/concepts/canonical-concept-name.md`)

```markdown
---
title_en: "Mixed-Initiative Interface"
title_zh: "主客協同介面"
tags: [interaction-technique, human-ai-collaboration, hci]
---

# Mixed-Initiative Interface (主客協同介面)

## 📖 概念定義 (Definition)
一種人機協作互動範式，電腦代理（Agent/AI）與人類使用者皆能主動發起對話、提出行動或接管任務，雙方基於各自優勢共同推進目標。

## 🧠 核心互動機制與設計原則 (Interaction Paradigm & Design Principles)
* **主導權動態切換**：系統在何種時機應由人類主導，何種時機由 AI 介入。
* **透明度與可解釋性**：AI 的每一次主動行動都必須對使用者保持可感知、可調整且可撤銷。

## ⚖️ 優缺點與使用者體驗權衡 (UX Tradeoffs)
| 維度 | 優勢 (Pros) | 挑戰 / 缺點 (Cons) |
| :--- | :--- | :--- |
| **工作效率** | 減少重複性手動操作，主動分擔認知負荷 | 容易因過度介入打斷使用者的專注心流（Flow） |
| **主觀控制感** | 讓使用者在享受自動化的同時維持控制感 | 若 AI 行為不透明，使用者會產生不信任感 |

## 📚 代表性論文 (Representative Papers)
* [[2024-chi-smith-generativecanvas|Smith et al., 2024 - Generative Canvas: Designing Mixed-Initiative Interfaces for Creative Writing]]
```

---

## 5. 標準操作流程 (Standard Operations)

### 操作 1：Ingest (收到 PDF 上傳時的自動處理)
當使用者在對話中上傳 PDF 論文時：
1. **識別與重命名**：
   * 讀取論文第 1 頁，解析出 `發表年份 (YYYY)`、`會議/期刊 (Venue)`、`第一作者 (FirstAuthor)`、`論文簡稱 (ShortTitle)`。
   * 將原始檔案以 `YYYY-Venue-FirstAuthor-ShortTitle.pdf` 規範儲存至 `raw/` 目錄。
2. **生成 HCI 專屬論文頁面**：在 `wiki/papers/` 建立符合模板的 Markdown 檔案。
3. **沉澱概念/互動技術頁面**：若論文提出了具代表性的新介面機制或設計範式，在 `wiki/concepts/` 建立或更新該概念頁。
4. **更新索引 (`index.md`)**：追加論文與概念條目。
5. **紀錄操作日誌 (`log.md`)**：追加如 `## [YYYY-MM-DD] ingest | 2024-CHI-Smith-GenerativeCanvas`。
6. **回報使用者**：回報重新命名後的檔案路徑、論文 TL;DR 與生成的 Wiki 頁面連結。

### 操作 2：Query (問答與橫向比較)
特別針對「**針對問題 X，有哪些主流的解決思路，各自的 Pros & Cons 是什麼？**」：
1. 檢索 `index.md`，找出所有嘗試解決「問題 X」或針對該使用者痛點的論文與互動技術。
2. 產出橫向對比矩陣：
   * 痛點與挑戰分析。
   * **不同互動方案 / 介面原型的對比表**（比較：互動範式、使用者控制感、認知負荷、適用場景、Pros & Cons）。
   * 統整各論文在 User Study 中歸納出的共通**設計指引（Design Implications）**。
3. 若成果具備長期參考價值，主動整理為綜合頁面沉澱回 Wiki。

### 操作 3：Lint (健康維護)
1. 檢查 `raw/` 內的 PDF 是否皆完成入庫與格式化命名。
2. 檢查 `wiki/` 內是否有失效連結或未在 `index.md` 列出的頁面。
3. 提示哪些互動範式已出現在多篇論文中，建議整合為概念專頁。

### 操作 4：Slide Generation (教學簡報生成 SOP —— 驗證左移與人機雙軌驗證)
針對作業或教學簡報產出，嚴格落實「三階段品質檢驗管線（Three-Stage Pipeline）」與「驗證左移（Shift-Left）」機制，杜絕直接跨階段寫代碼：

1. **階段一：大綱規劃與故事骨架 (Outline Generation)**
   * **執行**：強制以 Wiki 為 100% 知識來源，針對初學者心智模型規劃 8～15 頁大綱與敘事節奏。
   * **【人類檢查門 Gate 1 · 審方向】**：將大綱呈現給使用者審查故事切入點、篇幅與主題適配性。

2. **階段二：逐頁詳細腳本 (Slide-by-Slide Script)**
   * **執行**：大綱核准後，展開為純文字/Markdown 的逐頁詳細腳本（包含每頁副標題、敘事話術、生活案例、引用數據與卡片排版規劃）。
   * **【關鍵左移門 Gate 2 · 審內容】**：
     * **核心原則**：「大綱通過了，細節依然可能不滿意！」
     * 使用者在此純文字階段親自審查文字語氣、比喻貼切度與跨篇章融洽感。若發現某篇論文或段落跳脫主題（如過於生硬或偏向工程代碼），在此階段以極低成本即時退回修正或剔除，**嚴禁在未獲得逐頁內容核准前直接編寫 HTML 代碼**。

3. **階段三：HTML 程式碼實作與渲染 (Code Generation & UX Verification)**
   * **執行**：僅在逐頁腳本獲得人類確認後，才套用固定比例母版（`max-width: 980px; height: 680px; overflow-y: auto;`）生成單一 HTML 簡報，注入鍵盤導航、進度條與連續導覽按鈕。
   * **【體驗驗收門 Gate 3 · 審體驗】**：在瀏覽器中驗收翻頁是否固定無跳動、全域導航是否閉環。
