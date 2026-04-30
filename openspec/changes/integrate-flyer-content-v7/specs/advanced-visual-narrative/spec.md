## ADDED Requirements

### Requirement: 分段式標語視覺衝擊
系統必須透過分層排版與動畫，讓 Slogan 的「否定」與「肯定」部分產生強烈的視覺對比與出現時差。

#### Scenario: 標語動畫節奏
- **WHEN** 捲動進入 Scene 1
- **THEN** 「不是更努力」先以暗灰色顯示，隨後「系統與專業」部分以高亮度金色亮起。

### Requirement: 實體卡片感 QR Code 組件
系統必須將 QR Code 容器渲染為具備物理質感（陰影、高光、邊框、玻璃擬態）的卡片形式。

#### Scenario: 卡片視覺效果驗證
- **WHEN** 進入 Scene 3 的 Action 區域
- **THEN** QR Code 呈現出具備厚度感的白色玻璃卡片外觀，並帶有細緻的銀色/金色邊框。

### Requirement: 導讀點物理鑲嵌動畫
當導覽點（Guided Dot）移動至 QR Code 區域時，必須從圓形平滑變形為與卡片邊框一致的形狀，呈現「卡入」的視覺效果。

#### Scenario: 導讀點嵌入動畫
- **WHEN** 捲動百分比超過 88%（進入 QR 捕捉範圍）
- **THEN** 導讀點寬度增加、圓角減少，並與 QR Code 背景容器完美重合。
