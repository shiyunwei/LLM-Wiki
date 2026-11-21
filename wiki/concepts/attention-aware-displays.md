---
title_en: "Attention-Aware Displays & Disruptiveness Tradeoff"
title_zh: "注意力感知顯示與干擾性權衡"
tags: [hci, ambient-display, calm-technology, gamification, attention-management]
---

# Attention-Aware Displays & Disruptiveness Tradeoff (注意力感知顯示與干擾性權衡)

## 📖 概念定義 (Definition)
**注意力感知顯示器 (Attention-Aware Displays)** 是一類結合感測器（如人臉辨識、眼動追蹤、距離感測），能夠即時偵測使用者的注意力分配狀態，並據此動態調節資訊呈現方式與通知強度的智慧介面。其設計核心在於平衡「有效吸引與維持專注」與「避免對主要任務造成侵入性打擾（Disruptiveness）」之間的張力。

---

## 🧠 核心互動機制與設計原則 (Interaction Paradigm & Design Principles)

* **注意力漏斗推進 (The Audience Funnel)**：
  * 介面依據使用者狀態，流暢切換互動模態：
    1. **周邊漫不經心 (Inattention)** ➔ 透過邊界聲光微刺激（Gentle Notification）喚醒好奇心；
    2. **進入焦點 (Focused Attention)** ➔ 立即消除刺激，呈現核心資訊；
    3. **深度維持 (Retaining Attention)** ➔ 引入輕量遊戲化（進度反饋、成就解鎖）延長專注時長。
* **溫柔引導原則 (Lead Me Gently)**：
  * 轉換必須循序漸進，避免高分貝警報或突兀的全螢幕閃爍，保護使用者在公共或半公共空間的舒適心流。
* **干擾預算考量 (Interruption Budget)**：
  * 系統發送中斷提醒的頻率與強度，必須與當前環境情境匹配（等待情境可適度提高中斷以傳遞教育資訊，深度工作情境則應嚴格限制）。

---

## ⚖️ 優缺點與使用者體驗權衡 (UX Tradeoffs)

| 維度 | 優勢 (Pros) | 挑戰 / 缺點 (Cons) |
| :--- | :--- | :--- |
| **資訊到達率** | 顯著提早吸引使用者注意，知識吸收率倍增 | 容易因通知過度而被使用者標籤為「令人心煩的干擾」 |
| **互動自然度** | 隨使用者視線自適應調節，符合人體工學直覺 | 攝影機感測可能引發旁觀者的被拍攝隱私疑慮 |

---

## 📚 代表性論文 (Representative Papers)
* [[2014-compedu-borner-attentionawareambientdisplays|Börner et al., 2014 - Lead me gently: Facilitating knowledge gain through attention-aware ambient learning displays]]
