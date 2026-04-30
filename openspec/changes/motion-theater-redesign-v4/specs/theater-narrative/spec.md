## ADDED Requirements

### Requirement: 劇場式容器 (Theater Container)
網頁必須使用一個佔滿視窗的 `sticky` 容器，作為所有內容場景的舞台。

#### Scenario: 捲動網頁
- **WHEN** 使用者進行捲動
- **THEN** 舞台容器應保持在視窗固定位置，內容場景隨捲動進度進行切換，而非頁面位移

### Requirement: 數學軌跡引導點 (Math-Based Motion)
導讀點的座標必須透過純數學公式（如正弦波或貝茲曲線公式）動態計算，而非讀取外部路徑檔。

#### Scenario: 穩定追蹤
- **WHEN** 在不同解析度的手機或桌機上捲動
- **THEN** 導讀點應始終保持在預設的視覺安全區域內，不產生任何偏移或卡死

### Requirement: 場景序列化 (Scene Sequencing)
系統必須將捲動總長度劃分為不同的場景區間，並實作平滑的透明度與縮放過渡。

#### Scenario: 切換至專業項目
- **WHEN** 捲動進度達到 50%
- **THEN** 「理念」場景應淡出，同時「專業項目」場景應從縮放狀態平滑顯現

### Requirement: 聚焦磁吸感應 (Focus Magnetism)
當導讀點經過特定元素（如標題文字）時，該元素應產生朝向導讀點的微幅位移。

#### Scenario: 聚焦標題
- **WHEN** 導讀點移動至文字上方
- **THEN** 文字應產生感應式的縮放或位移，增加點與內容的交互感
