---
title_en: "Seamful Design"
title_zh: "縫隙設計"
tags: [hci, ubiquitous-computing, interaction-design, awareness-systems]
---

# Seamful Design (縫隙設計)

## 📖 概念定義 (Definition)
**縫隙設計 (Seamful Design)** 是普適運算（Ubiquitous Computing）與人機互動中的經典設計哲學。與傳統追求「無縫（Seamless）」、極力向使用者掩蓋底層技術缺陷或網路波折的觀點不同，縫隙設計主張**主動揭露並誠實展現系統在感知、通訊與運算邊界上的瑕疵與不確定性（Seams）**，並將這些「縫隙」轉化為增進使用者理解、調整心智模型與提升信任的互動線索。

---

## 🧠 核心互動機制與設計原則 (Interaction Paradigm & Design Principles)

* **坦露不確定性而非偽造完美**：
  * 在環境感知（Sensor-based）或 AI 推理中，漏報或誤判不可避免。系統透過機率性詞彙（如「長者『可能』在小睡」）取代武斷的確定句，並允許使用者隨時查閱訊號強度與感測器電量。
* **避免虛假警報帶來的恐慌**：
  * 若系統堅持無縫偽裝，一旦底層網路斷線或電池耗盡，系統產生的斷訊容易被使用者解讀為「發生嚴重意外」；透過展示技術縫隙，使用者能立即判斷是「機器故障」而非「長者出事」。

---

## ⚖️ 優缺點與使用者體驗權衡 (UX Tradeoffs)

| 維度 | 優勢 (Pros) | 挑戰 / 缺點 (Cons) |
| :--- | :--- | :--- |
| **信任維護** | 避免因系統黑箱誤判而徹底喪失使用者信任 | 暴露過多技術細節容易增加一般使用者的認知負擔 |
| **錯誤防護** | 使用者能感知系統邊界，不會過度依賴自動化 | 介面需要精心設計分層呈現（平常隱藏，需要時展開） |

---

## 📚 代表性論文 (Representative Papers)
* [[2008-ami-metaxas-dailyactivitiesdiarist|Metaxas et al., 2008 - Daily Activities Diarist: Supporting Aging in Place with semantically enriched narratives]]
