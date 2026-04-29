## ADDED Requirements

### Requirement: 沉浸式行動端 Hero 佈局
系統在行動裝置上應提供具備衝擊力的首屏視覺，利用文字描邊（Text Stroke）與照片的層疊關係營造深度感。

#### Scenario: 手機進入首頁
- **WHEN** 使用者使用手機開啟網頁
- **THEN** 系統應展示包含教練照片與大型描邊標題的沉浸式 Hero 區塊，標題應具備與背景照片的視差效果

### Requirement: 行動端卡片滑動 (Scroll Snap)
在行動裝置上，專業項目區塊應採用水平滑動或垂直停靠的卡片模式，確保使用者能直覺地瀏覽每一項專業。

#### Scenario: 手機瀏覽專業項目
- **WHEN** 使用者在手機上滑動專業項目區塊
- **THEN** 系統應自動停靠（Snap）至目前的專業卡片，並展示對應的說明文字

### Requirement: 元素進場動畫 (Reveal Animation)
網頁各主要區塊在進入使用者視野時，應具備平滑的進場動畫。

#### Scenario: 捲動至新區塊
- **WHEN** 使用者捲動網頁使新區塊進入視野
- **THEN** 系統應執行上浮、漸顯等動態效果，提升瀏覽的節奏感

### Requirement: 觸控互動優化
系統應偵測裝置類型，在觸控裝置上停用自定義游標，並強化點擊按鈕時的視覺回饋。

#### Scenario: 手機點擊預約按鈕
- **WHEN** 使用者在觸控螢幕上點選「BOOK SESSION」按鈕
- **THEN** 系統應隱藏電腦版的自定義游標，並在點擊瞬間提供微小的縮放（Scale）回饋

## MODIFIED Requirements

### Requirement: 響應式佈局 (RWD)
網頁必須在手機、平板與電腦上都能正常顯示，且行動端應具備專屬的「Premium」互動設計標準。

#### Scenario: 手機瀏覽網頁
- **WHEN** 使用者使用手機開啟網頁
- **THEN** 系統應自動調整版面為專為手機設計的單欄沉浸式排列，並啟用行動端特有的動效（如 Text Stroke 與 Reveal Animation）
