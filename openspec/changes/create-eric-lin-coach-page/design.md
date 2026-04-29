## Context

本專案旨在將 Eric Lin 教練的宣傳資訊從靜態圖片轉化為具備互動感與專業美學的網頁。專案目標是提供一個輕量、快速且具備高品質視覺效果的單頁式（Single-page）靜態 HTML。

## Goals / Non-Goals

**Goals:**
- **極簡維護**：採用單一 HTML 檔案架構，不依賴外部框架（如 React/Vue）。
- **視覺震撼**：參考 YGSC 的活力金黃風格，提供 Premium 級別的運動感設計。
- **高轉化率**：優化 QR Code 與預約按鈕的點擊路徑。
- **完全響應式**：針對手機瀏覽進行深度優化。

**Non-Goals:**
- 不包含後端預約管理系統（使用者直接跳轉 LINE）。
- 不包含部落格或多頁面結構。
- 不使用過重的 JavaScript 庫（如 jQuery）。

## Decisions

- **原生 CSS (Vanilla CSS)**：不使用 Tailwind 或 Bootstrap，以獲取最大的設計自由度並減少外部依賴。利用 CSS Variables 定義顏色系統（如 `--color-primary: #E9A805`）。
- **現代佈局技術**：使用 CSS Grid 與 Flexbox 構建佈局，確保在不同螢幕尺寸下的穩定性。
- **視覺效果與動態 (Ultra-Fancy)**：
    - **沈浸式 Hero**：採用全螢幕視差效果，教練硬舉照作為獨立圖層浮現。
    - **橫向捲動區塊**：利用 `sticky` 定位實作垂直捲動觸發橫向滑動的效果展示專長項目。
    - **3D 互動卡片**：使用 CSS `perspective` 與 `rotate3d` 實作滑鼠追蹤傾斜效果。
    - **動態背景文字**：使用動畫讓大型標題字在背景持續流動。
    - **慣性滾動與進場動畫**：實作 GSAP 風格的元素進入動畫。
- **資源管理**：由於是單檔案，圖片將採用本機路徑（或在需要時 Base64 編碼，視檔案大小而定）。

## Risks / Trade-offs

- **[Risk] 靜態 HTML 擴充性較低** → [Mitigation] 本專案定位為「個人名片」，後續若有大規模需求可再遷移至 Next.js 等框架。
- **[Trade-off] 單檔案 CSS 可能較長** → [Mitigation] 透過良好的 CSS 結構化注釋與變數定義來維持可讀性。
