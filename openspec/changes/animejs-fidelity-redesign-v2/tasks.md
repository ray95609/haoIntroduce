## 1. 幾何底層建設 (Geometric Foundation)

- [x] 1.1 在 HTML 中加入 `<canvas id="bg-canvas"></canvas>`。
- [x] 1.2 實作 Canvas 點陣繪製邏輯，使其支援隨捲動產生的視差位移。
- [x] 1.3 調整背景色與點陣顏色，使其符合 Anime.js 的極簡高對比風格。

## 2. 進階變形動畫 (SVG Morphing Intro)

- [x] 2.1 準備多組 SVG 路徑（從幾何方塊到字母邊框）。
- [x] 2.2 在 Anime.js Timeline 中實作開場的 Morphing 動效。
- [x] 2.3 強化字母組裝時的幾何線條繪製細節。

## 3. 全域交錯動效引擎 (Universal Stagger Engine)

- [x] 3.1 重新封裝 `IntersectionObserver` 邏輯，支援巢狀子元素的延遲進場。
- [x] 3.2 為「專業項目」與「理念文字」套用更細膩的 Stagger 參數。
- [x] 3.3 實作文字「逐字彈出」或「逐行彈出」的 Anime.js 配置。

## 4. 數據更新與 UI 拋光 (Data & Polish)

- [x] 4.1 更新 LINE 預約連結為 `https://line.me/ti/p/1VjR0jyXCu`。
- [x] 4.2 更新 QR Code 生成邏輯以匹配 new 連結。
- [x] 4.3 調整字體大小與間距，使其呈現出更具張力的設計排版。

## 5. 驗證與測試 (Verification)

- [x] 5.1 驗證 Canvas 背景在行動裝置上的捲動效能。
- [x] 5.2 確保所有動畫在捲動時不會產生重疊或殘影。
