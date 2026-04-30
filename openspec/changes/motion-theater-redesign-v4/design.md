## Context

目前的 V3 實作雖然具備基本動效，但其「長頁面」結構與「導讀點」的物理關聯性太弱，且座標容易失效。V4 將仿照 `motion.zajno.com` 的「劇場架構」，讓背景固定，內容隨捲動在中心舞台切換。

## Goals / Non-Goals

**Goals:**
- **場景式導讀**：將頁面內容切換為四個核心場景 (Hero, Story, Expertise, CTA)。
- **數學錨點軌跡**：使用穩定的數學公式計算點的座標。
- **視角聚焦**：內容始終繞著導讀點進行展開與收縮。

**Non-Goals:**
- 不再保留傳統的 HTML 滾動條視覺（雖然功能保留，但畫面將以舞台為主）。

## Decisions

- **Sticky Viewport 架構**：
    - **Rationale**: 透過 `body { height: 500vh }` 與內部 `position: sticky` 的舞台，我們可以精確控制捲動進度，並將其映射到場景切換上，避免傳統 RWD 造成的排版位移問題。
- **參數化軌跡運算 (Parametric Motion)**：
    - **Rationale**: 使用正弦函數 (Sine Wave) 與貝茲曲線公式動態生成 X/Y 座標。這能保證在任何螢幕比例下，導讀點都能精確落在視窗中心 60% 的黃金區域。
- **場景堆疊管理 (Scene Stacking)**：
    - 每個場景是一個 `z-index` 不同的層，根據 `scrollProgress` 決定其 `opacity` 與 `filter: blur()` 狀態。
- **行動端互動優化**：
    - 點的縮放與脈衝將與觸控速度掛鉤，增加「觸感」。

## Risks / Trade-offs

- **[Risk] SEO 爬蟲抓取問題** → [Mitigation] 確保所有內容仍存在於 DOM 中，僅透過 CSS 控制顯示，不使用全 JS 渲染。
- **[Risk] 結尾點擊失效** → [Mitigation] 在最後一個場景 (CTA) 時，將導讀點的 `z-index` 降低，或設定 `pointer-events: none`。
