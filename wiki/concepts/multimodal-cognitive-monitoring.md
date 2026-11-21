---
title_en: "Multimodal Cognitive State Monitoring"
title_zh: "多模態認知狀態監測"
tags: [hci, neuroergonomics, physiological-sensing, eeg, eye-tracking, cognitive-workload]
---

# Multimodal Cognitive State Monitoring (多模態認知狀態監測)

## 📖 概念定義 (Definition)
**多模態認知狀態監測 (Multimodal Cognitive State Monitoring)** 是指在人機互動與神經人因工程（Neuroergonomics）中，同步結合兩種或以上非侵入式生理感測技術（最典型為腦電圖 EEG 與眼動追蹤 Eye-Tracking），藉由大腦皮層電生理動態與視覺行為指標的相互校準，以高精度即時評估操作者心智負荷、疲勞、壓力、警覺性衰退及分心狀態的技術體系。

---

## 🧠 核心互動機制與設計原則 (Interaction Paradigm & Design Principles)

* **感測器優勢互補 (Sensor Complementarity)**：
  * **眼動追蹤 (ET)**：直接反映「外部環境的視覺注意力配置」（透過凝視熱區、瞳孔直徑、眨眼頻率），對任務環境變化反應迅速，但容易受環境光線干擾。
  * **腦電圖 (EEG)**：直接反映「內部認知資源的消耗與皮層喚醒水準」（透過 Theta/Alpha/Beta 頻段功率與波段比值），對深層認知狀態敏感。
* **狀態重疊消歧義 (Disambiguating Overlapping States)**：
  * 「高度心智負荷」與「極度疲勞」在單一指標（如凝視發散）常呈現相似特徵；多模態融合能結合瞳孔動態（負荷高時瞳孔放大，疲勞時縮小）與 EEG 波段進行精準分類。
* **自適應人機介面閉環 (Closed-loop Adaptive UI)**：
  * 當系統判定認知過載或嗜睡時，介面能自動觸發警示、收斂多餘干擾資訊或啟動半自動輔助接管。

---

## ⚖️ 優缺點與使用者體驗權衡 (UX Tradeoffs)

| 維度 | 優勢 (Pros) | 挑戰 / 缺點 (Cons) |
| :--- | :--- | :--- |
| **分類精度** | 實證準確率較單一感測器提升 10%～20%，誤報率低 | 穿戴設備配戴繁瑣，電極與校準要求影響生態效度 |
| **即時情境覺知** | 能在使用者發生操作失誤前進行前瞻預警 | 個體生理基線差異大，需動態自適應校準演算法 |

---

## 📚 代表性論文 (Representative Papers)
* [[2026-frontiers-rivasvidal-eegeyetrackingmonitoring|Rivas-Vidal et al., 2026 - Combining EEG and eye-tracking for cognitive and physiological states monitoring]]
