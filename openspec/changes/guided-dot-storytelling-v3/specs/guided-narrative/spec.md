## ADDED Requirements

### Requirement: 導航視覺錨點 (Guiding Visual Anchor)
網頁必須存在一個始終可見的「導讀點」，優先針對行動裝置寬度進行優化。在手機上，導讀點必須保持在螢幕水平中央 60% 的範圍內，避免被手指遮擋或超出視界。

#### Scenario: 行動裝置捲動
- **WHEN** 使用者在手機上捲動
- **THEN** 導讀點應沿著專為垂直螢幕設計的 SVG 路徑移動，路徑應避開螢幕極邊緣區域

### Requirement: 動態路徑映射 (Dynamic Path Mapping)
系統必須準確將捲動百分比（0-100%）映射到 SVG 路徑的長度上，確保導讀點與當前瀏覽內容同步。

#### Scenario: 捲動至特定區塊
- **WHEN** 捲動至「專業項目」區塊
- **THEN** 導讀點必須恰好移動至該區塊的視覺中心位置

### Requirement: 上下文感知反饋 (Context-Aware Feedback)
導讀點在經過不同重要性的資訊時，必須產生視覺上的形狀或顏色變化。

#### Scenario: 經過關鍵理念
- **WHEN** 導讀點移動至關鍵標題文字上
- **THEN** 導讀點應產生擴張脈衝 (Pulse) 或改變顏色，吸引使用者停頓閱讀

### Requirement: 敘事終點對焦 (Narrative Final Focus)
敘事旅程必須以導讀點與行動呼籲 (CTA) 結合為終點。

#### Scenario: 抵達網頁底部
- **WHEN** 使用者捲動至最後一個區塊
- **THEN** 導讀點應自動縮放並完美鑲嵌至 QR Code 的中心，暗示旅程的完成
