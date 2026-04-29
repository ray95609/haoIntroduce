## Why

目前 Eric Lin 教練網頁在行動裝置（手機）上的視覺呈現較為單調，且部分在電腦版上的「Fancy」效果（如自定義游標、橫向捲動）在觸控裝置上的體驗不佳。為了確保行動端使用者也能感受到 Premium 級別的品牌形象，需要針對 RWD 進行深度優化，引入專為手機設計的沉浸式動效。

## What Changes

- **行動端視覺重構**：
    - 優化 Hero 區塊在手機上的排版，使用更具衝擊力的編輯感文字（Editorial Typography）。
    - 停用行動端的自定義游標以提升流暢度。
    - 將原本「垂直觸發橫向」的捲動模式，改為更符合手機操作直覺的水平滑動卡片（Scroll Snap）或沉浸式垂直疊加卡片。
- **動態效果升級**：
    - 實作元素進場動畫（Reveal Animations），提升瀏覽時的動態感。
    - 引入文字描邊（Text Stroke）與視察（Parallax）背景效果。
    - 優化觸控回饋（Haptic-style CSS transitions）。
- **效能優化**：調整大型濾鏡與模糊效果在手機上的負載。

## Capabilities

### New Capabilities
- 無

### Modified Capabilities
- `coach-profile-page`: 升級行動端的 RWD 需求與沉浸式互動標準。

## Impact

- **修改檔案**：`index.html`。
- **影響範圍**：視覺層、CSS 媒體查詢邏輯、JS 事件監聽處理。
