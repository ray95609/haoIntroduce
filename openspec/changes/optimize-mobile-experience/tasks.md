## 1. 基礎與效能優化 (Foundation & Performance)

- [x] 1.1 在 CSS 中新增媒體查詢，針對行動端（`(hover: none)`）隱藏 `#cursor` 與 `#cursor-follower`。
- [x] 1.2 調整行動端的 `mesh-bg` 濾鏡數值，降低 `blur` 程度以提升效能。
- [x] 1.3 修正大標題 `clamp` 數值，確保在 360px 寬度下不溢出螢幕。

## 2. Hero 區塊視覺升級 (Hero Section Enhancement)

- [x] 2.1 為行動端 Hero 標題實作 `-webkit-text-stroke` 描邊效果。
- [x] 2.2 調整行動端 Hero 圖片與文字的層疊順序（z-index），營造空間感。
- [x] 2.3 實作輕量級視差效果，讓背景文字隨手機捲動有細微位移。

## 3. 專業項目展示重構 (Mobile Card Carousel)

- [x] 3.1 針對行動端重寫 `.gallery` 佈局，將 `display: flex` 改為橫向捲動容器。
- [x] 3.2 應用 `scroll-snap-type: x mandatory` 於容器，並在卡片應用 `scroll-snap-align: center`。
- [x] 3.3 隱藏捲動條並優化卡片間距，確保使用者一眼能看出可左右滑動。

## 4. 進場動畫與交互細節 (Interaction & Reveal)

- [x] 4.1 撰寫 `Intersection Observer` 腳本，監聽各區塊進入視口的狀態。
- [x] 4.2 定義 CSS `.reveal` 動畫類別（如 `opacity: 0; transform: translateY(30px)`）。
- [x] 4.3 為「BOOK SESSION」按鈕添加觸控時的 `:active` 縮放回饋。
- [x] 4.4 限制 3D 旋轉效果僅在具備滑鼠（hover: hover）的裝置觸發，優化行動端捲動。
- [x] 4.5 調整圖片 `object-position: center 20%`，確保行動端長條圖片顯示精華區域。

## 5. 驗證與測試 (Verification)

- [x] 5.1 在瀏覽器開發者工具中模擬多種手機尺寸進行驗證。
- [x] 5.2 確認行動端捲動流暢度（FPS）表現良好。
