## Context

V5 實現了劇場框架，V6 則是要強化敘事深度。透過「引力場」與「數位掃描」將導讀點與網頁內容進行深度綁定，創造出更具情感與專業感的互動體驗。

## Goals / Non-Goals

**Goals:**
- **敘事錨點**：讓導讀點具備引導視線的功能。
- **有機心跳**：賦予導讀點生命感。
- **技術感場景 2**：強化「專業診斷」的視覺語彙。

**Non-Goals:**
- 不增加外部 JS 庫（繼續使用 anime.js 與純數學運算）。

## Decisions

- **引力場混合邏輯 (Gravity Blending)**：
    - `targetPos = AmbientMath * (1 - focus) + AnchorPos * focus`
    - `focus` 值由捲動進度驅動，在各場景中心點達到最高值 (0.6 - 0.7)，確保「溫柔陪伴」而非死鎖。
- **心跳節奏數學模型**：
    - 使用雙重正弦波組合：`heartbeat = pow(sin(t), 12) + 0.5 * pow(sin(t - 0.5), 8)`。
    - 這種模型能產生「重跳-輕跳」的生理節奏感。
- **數位掃描組件**：
    - 為 `.expertise-item` 增加 `::after` 偽元素，實作螢光掃描線。
    - 掃描線使用 `mix-blend-mode: overlay` 增加融合感。
- **動態網格背景**：
    - 在 Canvas 渲染循環中加入 `drawGrid` 函數，使用透明度漸變在場景切換時淡入網格。

## Risks / Trade-offs

- **[Risk] 多個錨點同時存在時的座標跳動** → [Mitigation] 使用 `focus` 權重平滑過渡 (Easing)，確保點在錨點間移動時是平滑滑行。
- **[Risk] 大量 CSS 動畫造成的 GPU 負荷** → [Mitigation] 掃描線僅在 `scene.active` 時播放動畫。
