## ADDED Requirements

### Requirement: 互動式點陣背景 (Interactive Dot Grid)
網頁背景必須具備由無數小點組成的矩陣，且這些點必須隨使用者捲動產生視差位移或縮放，營造精密感。

#### Scenario: 捲動網頁
- **WHEN** 使用者捲動頁面
- **THEN** 背景點陣應產生與內容捲動方向一致但速度不同的位移 (Parallax Effect)

### Requirement: SVG 路徑變形動效 (Path Morphing)
開場動畫中，幾何框架必須具備平滑的路徑變形效果，從一個形狀轉化為另一個形狀。

#### Scenario: 開場序列執行
- **WHEN** 網頁載入
- **THEN** SVG 線條應從字母邊框平滑變形為裝飾性框架

### Requirement: 全域交錯進場規範 (Universal Staggering)
所有內容元素（段落、列表項、圖片）在進入視口時，必須套用 Anime.js 的交錯 (Stagger) 延遲，不得同時出現。

#### Scenario: 瀏覽專業項目區塊
- **WHEN** 捲動到專業項目區塊
- **THEN** 各個專業項目卡片應依序（例如間隔 100ms）彈出

## MODIFIED Requirements

### Requirement: 預約聯絡功能
系統必須引導使用者至教練的最新 LINE 帳號進行預約。

#### Scenario: 點擊預約按鈕
- **WHEN** 使用者點擊「BOOK SESSION」或掃描 QR Code
- **THEN** 系統必須導向 `https://line.me/ti/p/1VjR0jyXCu`
