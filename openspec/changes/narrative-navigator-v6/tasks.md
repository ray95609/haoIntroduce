## 1. 視覺與結構準備 (Visual & Structural Prep)

- [x] 1.1 為 `.expertise-item` 加入數位掃描線 CSS 與邊角裝飾 `::before/::after`。
- [x] 1.2 在 HTML 中為關鍵敘事區塊標註 ID 以便座標快取。
- [x] 1.3 更新 `dot-pulse` 的 CSS，準備對接新的心跳數學模型。

## 2. 導讀點引擎升級 (Navigator Engine Upgrade)

- [x] 2.1 實作座標快取邏輯，包含場景 1 標題與場景 2 項目中心點。
- [x] 2.2 在 `updateDot` 中加入 `gravityInfluence` 混合運算。
- [x] 2.3 實作「雙跳」心跳數學模型，並應用於 `dot-pulse` 的 `scale` 與 `opacity`。（V6.1 已調整：結尾 QR 階段自動關閉）

## 3. 場景 2 技術感增強 (Expertise Immersion)

- [x] 3.1 實作背景網格 `drawGrid` 函數並整合進 Canvas 渲染循環。
- [x] 3.2 實作場景 2 專屬的引力行為：點移動到當前閱讀的項目。
- [x] 3.3 最終整合測試，確保從加載到導讀、再到 QR 捕獲的完整敘事流暢度。（V6.1 已調整：移除背景亂線，保持潔淨感）
