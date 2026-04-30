## ADDED Requirements

### Requirement: 劇場式開場動畫
網頁載入時必須呈現一個具備設計感的開場序列，利用幾何圖形與文字的動態組裝吸引使用者注意力。

#### Scenario: 初次進入網頁
- **WHEN** 使用者開啟網頁
- **THEN** 系統應先顯示黑屏，並以幾何線條繪製 `ERIC LIN` 字母，最後背景照片透過遮罩擴張（Mask Expansion）優雅顯現

### Requirement: 敘事導向捲動體驗 (Scrollytelling)
網頁內容必須隨使用者捲動而有節奏地出現，而非靜態排列，讓瀏覽過程像是在讀一個視覺故事。

#### Scenario: 向下捲動瀏覽
- **WHEN** 使用者向下捲動
- **THEN** 系統應觸發背景幾何圖形位移、文字交錯彈出 (Staggered Animation) 以及內容區塊的沈浸式切換

### Requirement: 無溢出版面配置 (Zero-Overflow Layout)
網頁在任何螢幕尺寸下皆不得出現水平捲動軸，所有視覺元素必須限制在視窗寬度內。

#### Scenario: 手機版穩定性測試
- **WHEN** 使用者在手機上左右滑動網頁
- **THEN** 系統應鎖定水平位移，確保頁面只能垂直捲動，且底部內容完美居中

## MODIFIED Requirements

### Requirement: 響應式佈局 (RWD)
網頁必須在各裝置上提供一致的 Premium 體驗，行動端應具備專屬的敘事動效優化。

#### Scenario: 行動裝置瀏覽
- **WHEN** 使用者使用手機瀏覽
- **THEN** 系統應自動將敘事佈局調整為垂直窄版，並保留 Anime.js 核心動效，確保在觸控裝置上的流暢度與視覺震撼力
