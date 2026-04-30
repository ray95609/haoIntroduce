## Why

V4 雖然實現了劇場架構，但初始載入時的黑屏與「點位偏移」會讓使用者感到困惑。此外，故事的終點（QR Code）缺乏視覺上的儀式感。V5 旨在透過「能量啟動 (Energy Boot)」與「QR 捕獲 (QR Capture)」這兩個極具張力的環節，補齊體驗的開頭與結尾。

## What Changes

- **能量啟動加載器 (Energy Boot Loader)**：實作一個以導讀點為中心的加載進度系統，避免黑屏並確保點從一開始就在正確位置。
- **QR 能量捕獲 (QR Capture Conclusion)**：實作導讀點與 QR Code 的磁吸形變特效，讓點在結尾時「擴散並包圍」QR Code。
- **初始狀態修復 (Initialization Fix)**：確保導讀點在加載期間隱藏或鎖定在中心，轉場時再以動態方式進入軌跡。

## Capabilities

### New Capabilities
- `energy-loader`: 以點為中心的進度加載系統。
- `qr-capture`: 結尾場景的元素捕獲與形變邏輯。

### Modified Capabilities
- `theater-narrative`: 擴充場景 3 的收尾行為。

## Impact

- **視覺流程優化**：重寫 `loader` 結構與 JavaScript 的初始載入序列。
- **互動邏輯擴充**：在 `updateDot` 引擎中加入場景 3 的座標吸附與形變計算。
