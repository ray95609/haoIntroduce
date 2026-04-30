## Context

本階段旨在實作「行動優先 (Mobile-First)」的導讀點敘事。導讀點將作為垂直螢幕上的視覺中心，引導使用者完成品牌旅程。

## Goals / Non-Goals

**Goals:**
- **行動優先實作**：優先針對手機端（375px+）設計垂直導讀軌跡。
- **極致觸控流暢度**：優化行動端慣性捲動下的點位更新邏輯。
- **視覺引導**：透過點的位移減少行動端文字堆疊的沉悶感。

**Non-Goals:**
- 桌機版僅做為響應式的延展，不開發獨立的複雜橫向路徑。

## Decisions

- **行動端垂直路徑優化**：
    - **Rationale**: 手機螢幕窄長，路徑將設計為略帶曲線的垂直線，確保導讀點始終在使用者的大拇指操作區域與視線中心。
- **針對觸控慣性的 Lerp 補間**：
    - **Rationale**: 行動端的捲動具有慣性（Inertia），導讀點將使用較高的線性插值係數（0.15），使其跟隨感更為「黏手」且滑順。
- **動態 ViewBox 適應**：
    - 路徑 SVG 將使用 `preserveAspectRatio="xMidYMin slice"`，確保在不同長度的手機上路徑不會被過度拉伸。

## Risks / Trade-offs

- **[Risk] 路徑與內容對齊失效** → [Mitigation] 當視窗 resize 時重新計算路徑邊界，動態調整 SVG 的 viewBox。
- **[Risk] 手機端滑動干擾** → [Mitigation] 導讀點設定為 `pointer-events: none`，確保不影響使用者點擊。
