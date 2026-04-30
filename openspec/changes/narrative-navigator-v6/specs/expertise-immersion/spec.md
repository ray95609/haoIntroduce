## ADDED Requirements

### Requirement: 數位掃描線 (Digital Scan Line)
場景 2 (Expertise) 的每個專業項目卡片必須具備一條持續循環的水平掃描線，強化專業技術感。

#### Scenario: 進入場景 2
- **WHEN** 捲動進入場景 2
- **THEN** 專業項目卡片應出現螢光色的水平掃描線，由上至下循環移動

### Requirement: 背景數位網格 (Background Digital Grid)
在場景 2 (Expertise)，Canvas 背景應從自由線條轉變為數位網格模式。

#### Scenario: 場景切換中
- **WHEN** 場景 2 變為 Active
- **THEN** Canvas 背景應以漸變方式顯示數位網格線，並在導讀點經過時產生微小扭曲
