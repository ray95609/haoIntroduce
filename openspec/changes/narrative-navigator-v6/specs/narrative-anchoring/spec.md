## ADDED Requirements

### Requirement: 敘事引力場 (Narrative Gravity)
系統必須能夠定義「敘事錨點」，當使用者捲動至特定章節時，導讀點的座標應自動向該錨點偏移，擔任引航功能。

#### Scenario: 讀到介紹標題
- **WHEN** 捲動進度進入場景 1 (Intro)
- **THEN** 導讀點的數學路徑中心應自動向標題位置偏移

### Requirement: 溫柔路徑混合 (Smooth Gravity Blend)
導讀點在引力場中的運動必須維持「溫柔陪伴」感，座標應為數學隨機路徑與錨點座標的加權混合。

#### Scenario: 離開錨點區域
- **WHEN** 捲動進度離開特定的敘事錨點區間
- **THEN** 引力影響力應平滑降至 0，點回歸自由流動狀態
