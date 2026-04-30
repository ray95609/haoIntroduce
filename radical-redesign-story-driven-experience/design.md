## Context

本專案將打破既有的靜態網頁架構，採用「互動式導讀 (Scrollytelling)」模式重新打造 Eric Lin 的個人品牌頁面。目標是利用 Anime.js 的強大動效，讓網頁具備劇場般的進場與敘事感。

## Goals / Non-Goals

**Goals:**
- **視覺震撼力**：打造具備「Anime.js 靈魂」的高階動態效果。
- **敘事體驗**：使用者捲動時，內容像是在閱讀一個專業故事。
- **結構穩定**：解決所有 RWD 溢出問題，確保行動端完美呈現。

**Non-Goals:**
- 不保留舊有的 CSS 樣式，全面重寫以確保設計的一致性。
- 不使用過多的外部庫，僅依賴 Anime.js 提升動態品質。

## Decisions

- **Anime.js 核心驅動**：
    - **Rationale**: 原生 CSS 動畫在處理複雜的時間軸 (Timelines) 與交錯 (Staggering) 時較為吃力。Anime.js 提供精確的控制能力，適合實作開場的字母組裝與區塊切換。
- **全視窗疊加佈局 (Viewport-Fixed Layers)**：
    - 使用 `position: fixed` 鎖定背景視覺，透過捲動百分比觸發不同層級的內容顯現。
    - **Rationale**: 這種「捲動即劇情」的模式能創造更強的沈浸感，且能精確控制文字與圖片的重疊美感。
- **SVG Clip-path 遮罩轉場**：
    - 利用 `clip-path` 實作非線性的開場轉場。
    - **Rationale**: 相比於簡單的透明度變化，遮罩擴張能帶來更強大的視覺衝擊力，符合 Anime.js 的幾何美學。
- **主容器鎖定 (`overflow-x: hidden`)**：
    - 在 `body` 或 `#app-wrapper` 層級強制鎖定水平溢出。
    - **Rationale**: 這是解決 RWD 左右滑動問題的最直接、最穩定的方式。
- **混合模式 (Mix-blend-mode)**：
    - 文字在經過圖片時使用 `difference` 或 `overlay`。
    - **Rationale**: 增加視覺層次，讓背景文字與前景圖片產生高級的互動感。

## Risks / Trade-offs

- **[Risk] 動畫過多導致效能下降** → [Mitigation] 僅針對 `transform` 與 `opacity` 進行動畫處理，並在行動端簡化部分複雜的幾何補間。
- **[Trade-off] SEO 友好度** → [Mitigation] 確保所有內容在 HTML 中依然是語義化的，僅透過 CSS/JS 改變呈現方式。
