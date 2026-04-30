## Context

V4 的導讀點雖然能流暢遊走，但缺乏一個「起點」與「終點」的儀式感。V5 將透過強化 `loader` 的進度呈現與場景 3 的捕獲動效，來完善整個敘事鏈結。

## Goals / Non-Goals

**Goals:**
- **能量進度條**：在 Loader 期間提供明確的加載反饋。
- **點的初始鎖定**：確保點在加載完成前不會出現偏移。
- **QR 能量容器化**：在故事終點將點轉化為 QR Code 的強調框。

**Non-Goals:**
- 不進行真正的網路資源監控加載（採用模擬加載以保證視覺節奏）。

## Decisions

- **能量進度條實作**：
    - 在 `loader` 中加入一個 `svg` 圓環，其 `stroke-dashoffset` 與模擬進度掛鉤。
    - 導讀點在加載期間處於 `fixed` 中心，並與能量環產生共振。
- **QR Code 座標快取 (Coordinate Caching)**：
    - **Rationale**: 為了確保磁吸的精確性，我們在頁面載入與視窗調整 (Resize) 時，預先計算 QR Code 的中心座標並存入變數，避免在 `requestAnimationFrame` 中重複調用效能昂貴的 `getBoundingClientRect`。
- **狀態驅動的導讀點屬性**：
    - 使用一個 `state` 旗標來切換導讀點的行為：`FREE_FLOW` (場景 0-2) 與 `QR_SNAP` (場景 3)。
    - 在 `QR_SNAP` 狀態下，導讀點的 `border-radius` 與 `size` 將透過 CSS Transition 平滑過渡。

## Risks / Trade-offs

- **[Risk] 滾動過快導致磁吸不穩** → [Mitigation] 使用較強的 Lerp 係數 (0.2) 來處理磁吸階段的目標座標跟隨。
- **[Risk] 手機版座標偏移** → [Mitigation] 所有座標計算均相對於 `theater-stage` 容器而非 `body`。
