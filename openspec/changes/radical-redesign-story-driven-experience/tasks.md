## 1. 結構與依賴設定 (Structure & Setup)

- [x] 1.1 在 `index.html` 引入 Anime.js CDN 並建立全新的 HTML 骨架。
- [x] 1.2 設定主容器樣式，套用 `overflow-x: hidden` 徹底鎖定水平溢出。
- [x] 1.3 定義全新的 CSS 變數系統（色彩、字體、層級）。

## 2. 劇場式開場動畫 (The Cinematic Intro)

- [x] 2.1 實作黑屏 Loading 遮罩，並使用 SVG 繪製字母組裝動效。
- [x] 2.2 使用 Anime.js 實作首屏照片的 `clip-path` 擴張效果。
- [x] 2.3 實作開場文字的 Staggered (交錯) 彈出動畫。

## 3. 敘事流捲動引擎 (Storytelling Engine)

- [x] 3.1 建立捲動百分比監聽器，將滾動距離轉化為動態進度。
- [x] 3.2 實作背景幾何圖形隨捲動軌跡移動的動畫。
- [x] 3.3 設定區塊轉場邏輯，讓內容隨故事進度顯現或隱藏。

## 4. 內容整合與視覺拋光 (Content & Polish)

- [x] 4.1 將教練資訊（理念、專業項目、QR Code）整合進新佈局。
- [x] 4.2 應用 `mix-blend-mode: difference` 於標題文字，增加視覺深度。
- [x] 4.3 優化行動端的觸控滾動慣性與動畫流暢度。

## 5. 驗證與調校 (Verification)

- [x] 5.1 在行動裝置模擬器中確認「零溢出」狀態。
- [x] 5.2 進行效能分析，確保開場動畫在一般手機上不掉幀。
