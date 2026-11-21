---
title_en: "User Requirements for Technology to Assist Aging in Place: Qualitative Study of Older People and Their Informal Support Networks"
title_zh: "輔助在地安老之科技使用者需求：長者及其非正式支持網絡的質性研究"
year: 2018
venue: "JMIR Mhealth Uhealth 2018"
authors: "Phoebe Elers, Inga Hunter, Dick Whiddett, Caroline Lockhart, Hans Guesgen, Amardeep Singh"
raw_file: "raw/2018-JMIR-Elers-UserRequirementsAgingInPlace.pdf"
tags: [hci, qualitative-study, aging-in-place, informal-support, user-requirements]
---

# User Requirements for Technology to Assist Aging in Place (輔助在地安老之科技使用者需求)

## 📌 TL;DR
本研究針對過去智慧健康照護科技過度聚焦於「正式醫療體系」而忽略日常關鍵照護者的缺口，透過對 10 位獨居長者與 31 位「非正式支持網絡成員」（家人、朋友、鄰居）的深入質性訪談，提煉出推動科技輔助在地安老的三大主題與 15 項核心使用者需求，強調長者對資訊的主導控制權、異常狀況過濾通報以及避免科技取代真人溫度的重要性。

---

## 🎯 欲解決的使用者痛點與動機 (Motivation & User Need)
* **既有研究與系統盲點**：
  * 過去輔助長者在地安老（Aging in Place）的科技系統，大多專注於連接醫院或專業護理人員（Formal Support），但現實中 50%～90% 的日常照護責任實際上是由非正式支持網絡（Informal Support: 親友、子女、鄰居）承擔。
  * 系統往往將長者視為單一疾病患者，缺乏全人關懷，且容易因技術門檻、昂貴費用與隱私疑慮被長者束之高閣。
* **研究核心動機**：
  * 全面理解長者及其非正式支持網絡在溝通與安全監控上的真正資訊需求，以歸納出下一代智慧居家感知科技的原型設計指引。

---

## 👥 使用者研究與方法論 (User Study & Evaluation)
* **研究對象與方法**：
  * **受試者規模**：$N=41$（包含 10 位 70 歲以上且患有慢性病的獨居長者，以及 31 位被長者指定的非正式照護親友）。
  * **研究形式**：半結構化深入訪談（長者採面對面訪談，親友採面談、電話或 Skype），並使用 NVivo 進行紮根歸納式主題分析（Inductive Thematic Analysis）。

* **三大核心主題發現**：
  1. **社會賦能因素 (Social Enablers)**：
     * **採納時機點 (Timing)**：長者對監控科技的接受度高度取決於「臨界事件」（例如發生嚴重跌倒或認知退化跡象後，採納意願大幅提高）。
     * **親友的技術引導**：非正式網絡是長者學會並維持使用科技的核心推手。
  2. **技術疑慮 (Technology Concerns)**：
     * **經濟成本門檻**：退休長者收入有限，對昂貴的感測硬體極度敏感。
     * **生理機能退化**：視力衰退與手指關節不靈巧使得常規介面難以操作。
     * **科技冷漠恐懼**：強烈擔憂安裝監控設備後，親友會減少親自前來探望或泡茶的次數（*「設備可以告訴你發生了什麼事，但設備不能靠近幫她泡杯茶」*）。
  3. **期望的資訊型態 (Information Desired)**：
     * **異常例外通報 (Exception-based Reporting)**：照護者不需要被無意義的日常行為洗版，而需要在偏離常規時獲得通知（*「我不需要知道她今天開了 10 次冰箱；但如果她整天沒開，或者冰箱門一直沒關，我就需要知道」*）。

---

## 💡 設計啟發與指引 (Design Implications & Guidelines)

研究歸納出 15 項具體使用者需求（Table 1），其中最具 HCI 啟發的核心準則包括：

1. **資訊主控權必須回歸長者 (Elderly Control & Autonomy)**：
   * 長者必須能夠完全自主決定「哪些資訊被收集」、「何時被傳送」以及「開放給哪一位親友查看」（可針對不同親友設定不同授權等級）。
2. **常規過濾與異常通報機制 (Out-of-the-norm Processing)**：
   * 系統後端必須具備基礎行為模式學習能力，僅在活動「顯著異於日常作息」（如超時未起床、異常久坐、爐火超時未關）時才發送推播，降低照護者的警報疲勞，同時保護長者的日常尊嚴。
3. **借力現有家電，降低邊際成本與心理排斥**：
   * 盡量利用長者家中已有的電視、冰箱等現成家電附加非侵入式感測，減少昂貴專用硬體帶來的「我是病人」心理標籤。
4. **設計應促進而非取代實體互動**：
   * 介面設計應具備「社交觸發（Social Prompting）」機制，利用生活狀態引導子女主動發起探訪或溫暖通話，而非讓數據取代真實的人際溫度。

---

## 🔗 關聯概念與論文 (Related Concepts & Papers)
* **核心概念**：[[informal-support-networks|非正式支持網絡 (Informal Support Networks)]], [[peripheral-awareness|周邊感知系統 (Peripheral Awareness)]]
* **直接關聯論文**：[[2008-ami-metaxas-dailyactivitiesdiarist|Metaxas et al., 2008 - 日常生活日記感知系統]]
