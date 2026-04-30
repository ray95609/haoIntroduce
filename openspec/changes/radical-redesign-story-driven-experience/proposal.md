## Why

目前的網頁設計雖然具備基礎功能，但缺乏使用者要求的「沈浸式故事感」與「Anime.js 風格」的動態美學。此外，行動端存在的左右晃動問題影響了 Premium 品牌的專業感。本次改動將拋棄既有佈局，重新打造一個具備劇場感、故事導向的教練形象頁面。

## What Changes

- **視覺風格徹底重構 (BREAKING)**：
    - 引入 Anime.js 驅動的開場動畫與幾何圖形補間效果。
    - 改用「敘事流 (Storyline)」佈局，將教練的理念、專業與行動呼籲整合為一個連貫的視覺故事。
    - 實作高度沈浸式的首屏開場（黑屏解構到內容展開）。
- **佈局優化**：
    - 使用 `overflow: hidden` 的主容器徹底解決行動端左右晃動的問題。
    - 採用非對稱式、具備動態遮罩 (Clip-path) 的現代排版。
- **互動體驗升級**：
    - 實作隨捲動路徑變化的 SVG 動畫（Scrollytelling）。
    - 優化 staggered (交錯) 的文字出現效果，模仿 Anime.js 的流暢感。

## Capabilities

### New Capabilities
- 無

### Modified Capabilities
- `coach-profile-page`: 重新定義網頁為「敘事型沈浸式體驗」，提升視覺與動態要求。

## Impact

- **修改檔案**：`index.html` (內容將被完全覆蓋)。
- **外部依賴**：引入 `anime.js` (透過 CDN)。
