## Why

V3 的實作因為過度依賴複雜的 SVG Path 映射，導致在不同裝置上出現座標偏移與「點被卡住」的情況，無法達成 `motion.zajno.com` 那種沈浸式的導讀感。V4 將採用更激進的「劇場舞台 (Theater-Stage)」架構，徹底解決座標問題，並創造出極致流暢的敘事體驗。

## What Changes

- **劇場舞台架構 (Theater-Stage Layout)**：將網頁轉化為一個固定的舞台（Sticky Viewport），內容隨捲動在舞台中進行切換，而非傳統的垂直長頁面。
- **數學驅動引導點 (Math-Driven Anchor)**：捨棄不穩定的 SVG Path，改用純數學三角函數定義導讀點的運動軌跡，確保在任何解析度下都能精準運行。
- **場景淡入淡出 (Scene Transitions)**：捲動不再是位移，而是觸發不同「場景」的漸變與縮放，讓導讀點始終保持在視覺中心。
- **聚焦透鏡效果 (Focus Lens)**：導讀點將具備更強的「透鏡」感，當它移動到特定內容上時，會產生動態放大與強調效果。

## Capabilities

### New Capabilities
- `theater-narrative`: 實作基於 `sticky` 定位的劇場引擎與純數學軌跡運算。

### Modified Capabilities
- `guided-narrative`: 廢棄原有的 SVG Path 邏輯，轉向數學模型驅動。

## Impact

- **核心架構重寫**：`index.html` 的 DOM 結構將從「長度堆疊」改為「深度疊加」。
- **邏輯重構**：全面更新 JavaScript 的捲動映射邏輯。
