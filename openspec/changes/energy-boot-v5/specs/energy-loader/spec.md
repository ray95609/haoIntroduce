## ADDED Requirements

### Requirement: 中心能量啟動 (Centered Energy Boot)
Loader 必須將導讀點鎖定在螢幕正中心，並在其周圍顯示一個隨加載進度變化的能量環與百分比。

#### Scenario: 網頁加載中
- **WHEN** 網頁資源正在載入
- **THEN** 畫面應顯示中心導讀點與旋轉的能量環，進度百分比應從 00% 跳動至 100%

### Requirement: 啟動脈衝轉場 (Boot Pulse Transition)
當加載達到 100% 時，Loader 應觸發一個從中心擴散的脈衝動畫，隨後場景開始切換。

#### Scenario: 加載完成
- **WHEN** 進度達到 100%
- **THEN** 導讀點應產生一次強烈脈衝，Loader 消失，導讀點開始其數學軌跡運動
