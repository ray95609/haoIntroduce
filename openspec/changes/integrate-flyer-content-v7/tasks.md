## 1. Scene 1: Slogan 深化實作

- [x] 1.1 修改 `index.html` 中的 `#scene-hero` 與 `#scene-intro` 文案，結構化為分段 Span。
- [x] 1.2 在 CSS 中定義 `.slogan-not-effort` (暗灰色) 與 `.slogan-system` (金色) 樣式。
- [x] 1.3 更新 `updateScenes` 邏輯，加入 Slogan 的文字亮滅動畫時差。

## 2. Scene 2: 專業支柱豐富化

- [x] 2.1 更新 `#exp-1`, `#exp-2`, `#exp-3` 的標題與描述文案。
- [x] 2.2 在 CSS 中為 `.expertise-item` 增加隱藏的專業標籤樣式。
- [x] 2.3 加入光點停留在特定項目時的視覺微動特效（雷射掃描感強化）。

## 3. Scene 3: QR Code 與光點鑲嵌

- [x] 3.1 重新設計 QR Code 容器的 CSS，實作 Glassmorphism 與實體卡片質感。
- [x] 3.2 加入卡片邊緣的高光（Metallic highlight）與深層陰影效果。
- [x] 3.3 調校 `updateDot` 中的 morph 參數，確保進入 88% 捲動區時，光點與卡片的物理貼合感。

## 4. 驗證與拋光

- [x] 4.1 測試不同捲動速度下，Slogan 翻轉動畫的流暢度。
- [x] 4.2 檢查行動版裝置上的 QR 卡片排版。
- [x] 4.3 確保傳單文案無誤字並符合 Eric Lin 品牌語氣。
