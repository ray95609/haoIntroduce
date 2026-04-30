## Why

雖然 V2 版本在視覺精密度上已有顯著提升，但目前的滾動體驗仍偏向傳統的區塊切換。為了創造更強的導讀感與「一氣呵成」的敘事體驗，V3 將引入受 `motion.zajno.com` 啟發的「導讀點」機制，透過一個視覺錨點引導使用者完成整場品牌旅程。

## What Changes

- **導讀點機制 (The Guided Dot)**：引入一個在網頁中穿梭的螢光點，作為使用者的目光焦點。
- **SVG 路徑導航 (Path Navigation)**：定義一條隱形的幾何路徑，導讀點將隨捲動進度沿著此路徑移動。
- **互動式導讀 (Interactive Guiding)**：當導讀點接近特定內容（如專業項目或 QR Code）時，該元素會產生感應式的動態反饋（如發光、微幅晃動）。
- **沈浸式場景切換**：背景與文字的進場時機將與導讀點的座標位置緊密連動。

## Capabilities

### New Capabilities
- `guided-narrative`: 管理導讀點的路徑定義、捲動映射與跨區塊互動邏輯。

### Modified Capabilities
- `coach-profile-page`: 更新區塊轉場邏輯，使其支援基於導讀點位置的觸發機制。

## Impact

- **修改檔案**：`index.html`。
- **新增技術**：`anime.path()` 應用與 SVG Path 定義。
