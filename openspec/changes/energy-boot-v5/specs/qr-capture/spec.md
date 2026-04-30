## ADDED Requirements

### Requirement: QR 磁吸捕獲 (QR Magnetic Snap)
在最後一個場景 (Action Scene)，導讀點必須停止隨機遊走，並精確吸附到 QR Code 的中心座標。

#### Scenario: 捲動至結尾
- **WHEN** 捲動進度超過 90%
- **THEN** 導讀點的目標座標應自動鎖定為 QR Code 的中心位置

### Requirement: QR 能量圍繞 (QR Energy Surround)
當導讀點吸附到 QR Code 後，其形狀應從點擴散為一個包圍 QR Code 的發光方框。

#### Scenario: 完成捕獲
- **WHEN** 導讀點到達 QR Code 中心
- **THEN** 其寬高應迅速擴張（如 200px），`border-radius` 應減少以匹配 QR Code 的圓角，並形成一個呼吸感的外框
