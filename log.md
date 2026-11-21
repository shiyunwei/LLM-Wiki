# 系統操作日誌 (Wiki Operations Log)

本檔案為追加寫入（Append-only）的操作紀錄。格式固定為：
`## [YYYY-MM-DD] <operation> | <target>`
方便日後快速追溯與檢視。

---

## [2026-11-21] update | 更新 AGENT.md 簡報生成 SOP（加入逐頁內容人類審查與驗證左移機制）
* 在 [AGENT.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/AGENT.md) 正式確立「操作 4：Slide Generation」三階段檢驗管線。
* 將驗證嚴格左移：在大綱通過後，必須先產出純文字逐頁腳本供人類審查（Gate 2 · 審內容），確認無跳脫主題後方可進入 HTML 代碼生成（Gate 3 · 審體驗）。

## [2026-11-21] slides | 重構旗艦主題教學簡報《不打擾的溫柔：走進「平靜科技」與同理心人機互動》（00-synthesis-overview.html）
* **教學主題深耕與連貫故事化重構**：
  * 確立旗艦主題《不打擾的溫柔：走進「平靜科技」與同理心人機互動》（共 12 頁），採「起承轉合」四幕式敘事，完整銜接生活困境、平靜科技定義、生活實踐、極限守護、縫隙設計哲學與未來典範轉移。
  * 深入提煉注意力互動光譜（邊緣感知、焦點調取、自適應防護），全面聚焦於環境感知、長輩尊嚴與情感陪伴。
  * 嚴格落實固定卡片比例（`980x680px`）、`[ 🏠 回首頁 ]`、動態頁碼與全鍵盤翻頁支援。
  * 同步更新 [slides/index.html](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/slides/index.html) 頂部主題教學特刊橫幅與 [index.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/index.md) 索引。

## [2026-11-21] slides | 新增雙向串聯導覽（回首頁/下一篇）並移除實作技術贅詞
* **全局導覽無縫串聯**：
  * 在 5 份獨立簡報頂部全面加入 `[ 🏠 回首頁 ]` 與 `[ 下一篇 ➔ ]` 快速跳轉按鈕。
  * 在每份簡報的最後一頁加入直達下一份簡報的專屬按鈕（最後一篇連回總覽首頁），形成完整且連貫的閱讀路徑閉環。
* **首頁資訊精煉純化**：
  * 移除 [slides/index.html](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/slides/index.html) 中關於「手帳粉彩、單一HTML、鍵盤翻頁」等實作細節贅詞，純化為聚焦於研究學術主題的資訊列（核心文獻、沉澱概念、研究維度）。
* **動態頁數與比例保持**：
  * JavaScript 改為動態偵測實際投影片數量（`document.querySelectorAll('.slide-content').length`），讓內容依照論文需要自由增刪。
  * 嚴格保持固定比例卡片尺寸（`height: 680px`），確保翻頁穩定性。

## [2026-11-21] slides | 鎖定所有簡報卡片尺寸與比例，徹底消除翻頁跳動
* 針對 5 份獨立 HTML 簡報進行 CSS 結構最佳化：
  * 將 `.deck-wrapper` 統一鎖定為固定高度 `height: 680px` 與最大寬度 `max-width: 980px`，使翻頁時視窗尺寸、導覽按鈕與進度條位置絕對穩定，不再忽大忽小。
  * 內容區塊加上 `overflow-y: auto` 與客製化細緻滾動條，確保在任何解析度下內容完整呈現且不破壞整體卡片外觀。

## [2026-11-21] slides | 完成全套 5 份獨立 HTML 教學簡報與導覽入口網頁
* 嚴格依據 Wiki 知識庫內容，全面產出 5 份各自獨立的 11 頁溫柔手帳風 HTML 教學簡報：
  1. [01-metaxas-2008-daily-activities-diarist.html](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/slides/01-metaxas-2008-daily-activities-diarist.html)（日常生活日記 · 11 頁）
  2. [02-borner-2014-attention-aware-ambient-displays.html](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/slides/02-borner-2014-attention-aware-ambient-displays.html)（候診室無聲老師 · 11 頁）
  3. [03-elers-2018-user-requirements-aging-in-place.html](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/slides/03-elers-2018-user-requirements-aging-in-place.html)（長輩的真心話 · 11 頁）
  4. [04-shakeri-2023-sensing-their-presence.html](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/slides/04-shakeri-2023-sensing-their-presence.html)（五感被動相聚學 · 11 頁）
  5. [06-rivasvidal-2026-eeg-eyetracking-monitoring.html](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/slides/06-rivasvidal-2026-eeg-eyetracking-monitoring.html)（看透疲勞的大腦與眼睛 · 11 頁）
* 更新並啟動簡報總覽入口網頁 [slides/index.html](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/slides/index.html)，5 張卡片全數亮起綠燈完成狀態，可一鍵直達各份簡報。

## [2026-11-21] slides | 建立教學簡報總覽入口網頁與第 4 篇示範簡報
* 建立簡報總覽入口首頁 [slides/index.html](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/slides/index.html)（收錄 5 份獨立簡報之導覽卡片、統計與 Wiki 回連）。
* 產出候選 A 示範簡報 [04-shakeri-2023-sensing-their-presence.html](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/slides/04-shakeri-2023-sensing-their-presence.html)（11 頁，溫柔可愛手帳風，支援鍵盤左右鍵翻頁與進度條）。

## [2026-11-21] ingest | 批次讀入第二批 3 篇文獻，全庫達 5 篇完成作業標準
* **讀入論文**：
  1. `2014-CompEdu-Borner-AttentionAwareAmbientDisplays`：建立 [2014-compedu-borner-attentionawareambientdisplays.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/wiki/papers/2014-compedu-borner-attentionawareambientdisplays.md)。
  2. `2023-CHI-Shakeri-SensingTheirPresence`：建立 [2023-chi-shakeri-sensingtheirpresence.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/wiki/papers/2023-chi-shakeri-sensingtheirpresence.md)。
  3. `2026-Frontiers-RivasVidal-EEGEyeTrackingMonitoring`：建立 [2026-frontiers-rivasvidal-eegeyetrackingmonitoring.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/wiki/papers/2026-frontiers-rivasvidal-eegeyetrackingmonitoring.md)。
* **沉澱概念頁**：
  * [passive-co-presence.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/wiki/concepts/passive-co-presence.md) (被動共在感)
  * [multimodal-cognitive-monitoring.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/wiki/concepts/multimodal-cognitive-monitoring.md) (多模態認知狀態監測)
  * [attention-aware-displays.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/wiki/concepts/attention-aware-displays.md) (注意力感知顯示與干擾性權衡)
* **同步更新**：[index.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/index.md)（已索引 5 篇論文、6 個概念）。

## [2026-11-21] ingest | 批次讀入 2 篇 HCI 核心文獻並建立概念庫
* **讀入論文**：
  1. `2008-AmI-Metaxas-DailyActivitiesDiarist`：建立 [2008-ami-metaxas-dailyactivitiesdiarist.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/wiki/papers/2008-ami-metaxas-dailyactivitiesdiarist.md)。
  2. `2018-JMIR-Elers-UserRequirementsAgingInPlace`：建立 [2018-jmir-elers-userrequirementsaginginplace.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/wiki/papers/2018-jmir-elers-userrequirementsaginginplace.md)。
* **沉澱概念頁**：
  * [seamful-design.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/wiki/concepts/seamful-design.md) (縫隙設計)
  * [peripheral-awareness.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/wiki/concepts/peripheral-awareness.md) (周邊感知系統)
  * [informal-support-networks.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/wiki/concepts/informal-support-networks.md) (非正式支持網絡)
* **同步更新**：[index.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/index.md) 索引目錄。

## [2026-11-21] update | 更新為 HCI 專屬架構與自動命名 SOP
* 將 [AGENT.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/AGENT.md) 升級為人機互動（HCI）專屬結構。
* 確立 PDF 檔案自動重新命名規則：`YYYY-Venue-FirstAuthor-ShortTitle.pdf`。
* 新增 HCI 核心模組：使用者痛點 (User Need)、互動系統與原型 (System Prototype)、使用者研究 (User Study: $N$、量化/質性回饋、User Quotes) 及設計指引 (Design Implications)。
* 同步更新 [index.md](file:///c:/Users/shiyu/Desktop/115-1課程/生成式%20AI/LLM%20Wiki/index.md) 索引欄位以支援 HCI 特徵。

## [2026-11-21] init | 初始化論文 LLM Wiki 架構與規範 (AGENT.md)
* 建立基礎目錄結構：`raw/`、`wiki/papers/`、`wiki/concepts/`。
* 設定初始索引 `index.md` 與規範檔案 `AGENT.md`。
