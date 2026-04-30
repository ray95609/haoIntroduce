## Why

目前的重構雖然實作了基礎動畫，但在視覺密度與互動細節上尚未達到 `animejs.com` 官網的高水準。為了進一步提升 Eric Lin 品牌的專業感與技術感，V2 提案將聚焦於「幾何精密互動」與「高保真動效實作」。

## What Changes

- **動態點陣背景 (Interactive Dot Grid)**：實作一個隨捲動與滑鼠位移產生感應的點陣背景，模仿 Anime.js 官網的精密感。
- **進階開場序列 (Morphing Intro)**：利用 SVG 路徑變形 (Morphing) 實作更具流暢感的字母與幾何框架組裝。
- **全域交錯動效 (Staggered Everything)**：不僅是標題，所有列表、描述、按鈕都將套用精確的 Anime.js 交錯延遲進場。
- **QR Code 更新**：將 LINE 預約連結更新為 `https://line.me/ti/p/1VjR0jyXCu`。

## Capabilities

### New Capabilities
- 無

### Modified Capabilities
- `coach-profile-page`: 新增「幾何密度」與「互動式點陣背景」的視覺規範。

## Impact

- **修改檔案**：`index.html`。
- **動效邏輯**：大幅強化 JS 中的 Anime.js 控制邏輯。
