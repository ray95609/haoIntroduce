## Context

目前的 `index.html` 雖然具備基礎的 RWD，但在手機端的互動感較弱。本設計旨在透過現代 CSS 與輕量 JS，將桌面版的「Fancy」元素轉化為適合觸控與小螢幕的沉浸式體驗。

## Goals / Non-Goals

**Goals:**
- **提升行動端 Premium 感**：透過文字描邊與層疊效果提升視覺深度。
- **直覺互動**：使用符合手機直覺的 Scroll Snap 與觸控回饋。
- **效能平衡**：確保在手機上執行複雜 CSS 動效時依然流暢。

**Non-Goals:**
- 不引入外部 JS 庫（如 GSAP），維持單一檔案架構。
- 不改變基本的內容結構，僅優化呈現方式。

## Decisions

- **行動端專屬 Typography (Text Stroke)**：
    - 在行動端 Hero 區塊使用 `-webkit-text-stroke`。
    - **Rationale**: 手機螢幕較小，實心大字容易顯得擁擠，描邊文字可以在不遮擋背景照片的情況下維持標題的視覺重量。
- **Intersection Observer 觸發進場動畫**：
    - 使用原生 JS `Intersection Observer` 監聽區塊進入狀態，切換 `.is-visible` 類名來觸發 CSS `transition/animation`。
    - **Rationale**: 相比於監聽 `window.scroll` 事件，`Intersection Observer` 對效能更友善，能確保動畫在正確的時機觸發。
- **Scroll Snap 專業項目展示**：
    - 針對行動端，將 `.gallery` 的佈局從垂直捲動改為水平 `overflow-x: auto`，並應用 `scroll-snap-type: x mandatory`。
    - **Rationale**: 在手機上，左右滑動（Swipe）比垂直捲動（Scroll）更適合展示平行層級的卡片資訊。
- **偵測 `(hover: none)` 停用游標**：
    - 使用 CSS `@media (hover: none)` 與 JS `matchMedia` 判斷裝置類型。
    - **Rationale**: 觸控裝置沒有游標，硬要在上面渲染 `#cursor` 會造成效能浪費且影響體驗。
- **效能優化 (Filter reduction)**：
    - 在行動端降低 `mesh-bg` 的 `blur` 半徑，並簡化 `noise` 濾鏡。
    - **Rationale**: 高斯模糊（Blur）是非常耗費 GPU 資源的操作，手機端適度降低數值可顯著提升流暢度。

## Risks / Trade-offs

- **[Risk] 不同手機瀏覽器的 Scroll Snap 行為差異** → [Mitigation] 使用標準 CSS 屬性，並在 Android/iOS 主流瀏覽器上進行基本測試。
- **[Trade-off] CSS 複雜度增加** → [Mitigation] 透過清晰的 Media Query 區塊將手機版樣式集中管理。
