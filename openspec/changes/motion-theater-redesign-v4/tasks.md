## 1. 劇場架構建設 (Theater Scaffolding)

- [x] 1.1 修改 HTML 結構，引入 `.theater-stage` 容器與 `body` 的長度佔位。
- [x] 1.2 重新定義場景層 (Scene Layers)，將現有內容分配至四個場景。
- [x] 1.3 調整 CSS 確保場景在固定舞台中能完美對齊中心。

## 2. 數學動力引擎 (Math Motion Engine)

- [x] 2.1 實作基於 `requestAnimationFrame` 的數學座標運算（Sine/Cos 混合路徑）。
- [x] 2.2 實作導讀點的 Lerp 平滑化，確保在行動裝置上的滑順感。
- [x] 2.3 加入導讀點的視覺變形（Scale/Stretch）邏輯。

## 3. 場景切換邏輯 (Scene Transition Logic)

- [x] 3.1 實作捲動進度映射器，精確控制每個場景的 `opacity` 與 `transform` 曲線。
- [x] 3.2 實作場景切換時的「點擊穿透」管理，確保末尾 QR Code 可被點擊。

## 4. 聚焦與感應 (Focus & Interaction)

- [x] 4.1 加入場景進入時的導讀點脈衝 (Pulse) 回饋。
- [x] 4.2 實作內容元素的磁吸 (Magnetic) 位移邏輯。

## 5. 最終驗證 (Final Verification)

- [x] 5.1 測試在不同寬度手機上的場景適配性。
- [x] 5.2 驗證在「省電模式」或低功率行動裝置下的運行幀率。
