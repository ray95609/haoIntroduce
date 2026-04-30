## Why

V5 建立了基礎架構，但敘事過程仍顯「被動」。V6 旨在將導讀點進化為「主動導航者 (Active Navigator)」，並透過數位掃描特效強化場景 2 (Expertise) 的氛圍，營造出高端健身診斷的專業感。

## What Changes

- **敘事引力場 (Narrative Anchoring)**：實作引力邏輯，讓導讀點在捲動時能「溫柔地」被關鍵文字吸引，擔任引路功能。
- **心跳呼吸燈 (Heartbeat Rhythm)**：為導讀點加入持續且有機的雙跳心跳脈衝。
- **專業場景數位化 (Expertise Immersion)**：為場景 2 加入數位掃描線、邊角括號 `[ ]` 以及背景網格系統切換。

## Capabilities

### New Capabilities
- `narrative-anchoring`: 基於元素位置的動態路徑影響邏輯。
- `heartbeat-pulse`: 持續性的心跳節奏產生器。
- `expertise-immersion`: 場景 2 的數位 UI 元素與背景網格渲染。

### Modified Capabilities
- `math-motion-engine`: 擴充座標計算邏輯以支持引力偏移。

## Impact

- **腳本邏輯重構**：更新 `updateDot` 與 Canvas 渲染循環。
- **視覺組件更新**：新增場景 2 的 CSS 掃描線與裝飾性 UI。
