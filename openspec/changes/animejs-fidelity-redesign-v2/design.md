## Context

本階段旨在深度模仿 `animejs.com` 的視覺與互動邏輯。目前的設計在細節精度（幾何圖形數量、交錯動效的細膩度）上仍有提升空間。

## Goals / Non-Goals

**Goals:**
- **極致細節**：加入點陣背景與路徑變形，還原 Anime.js 官網的精密感。
- **動態一致性**：確保所有元素都遵循同一套交錯 (Stagger) 邏輯。
- **資訊準確**：更新 LINE 連結與 QR Code。

**Non-Goals:**
- 不引入額外的滾動庫（如 ScrollMagic），堅持使用原生的 `IntersectionObserver` 搭配 Anime.js 以保持輕量。

## Decisions

- **Canvas 點陣背景**：
    - **Rationale**: 使用數千個 DOM 元素來製作點陣背景會嚴重拖慢手機效能。改用 `<canvas>` 作為背景層，並在 JS 中計算點的位移。這能確保在維持高密度的同時，FPS 依然穩定。
- **SVG Morphing 時間軸**：
    - **Rationale**: 字母 `E`, `R`, `I`, `C` 將不再只是出現，而是從簡單的幾何方塊「變形」而成。這需要準備多組 SVG Path Data 並利用 Anime.js 的 `d` 屬性補間功能。
- **階層式 Stagger 邏輯**：
    - **Rationale**: 定義一個全域的 `staggerConfig`，確保標題、描述、項目的延遲時間具有比例感，營造出節奏感。
- **QR Code 數據更新**：
    - 將數據來源更新為 `https://line.me/ti/p/1VjR0jyXCu`。

## Risks / Trade-offs

- **[Risk] Canvas 繪製對電池的消耗** → [Mitigation] 僅在可見區域進行繪製，且當頁面停止捲動時降低更新頻率。
- **[Risk] SVG Morphing 兼容性** → [Mitigation] 確保所有 Path 點數一致，避免在某些瀏覽器產生扭曲。
