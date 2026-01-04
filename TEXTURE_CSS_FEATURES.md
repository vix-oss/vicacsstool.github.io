# Texture.css 功能列表 - index.html 整合

本文件列出了從 `texture.css` 整合到 `index.html` 的所有功能模組和可自訂選項。

## 新增功能模組 (10個)

### 1. 📋 主選單容器 (Everything Menu)
- **選擇器**: `.EverythingMenuContainer .EverythingMenu`
- **可自訂參數**:
  - 漸層角度 (0-360°)
  - 漸層起始顏色
  - 漸層結束顏色
  - 邊框顏色
  - 邊框半徑

### 2. ⚙️ 設定選單右側 (Settings Menu Right)
- **選擇器**: `.SettingsMenuRightInner .SettingBox`
- **可自訂參數**:
  - 背景漸層
  - 邊框顏色
  - 邊框半徑
  - 陰影效果

### 3. 🏠 選單側邊欄 (Menu Container)
- **選擇器**: `.Menu .MenuSideBar .MenuSideBarBody .MenuSideBarBodyTab`
- **可自訂參數**:
  - 邊框顏色
  - 亮度調整 (0-200%)
  - 背景圖片網址

### 4. 👍 點讚按鈕 (Like Button)
- **選擇器**: `.LikeButton`
- **可自訂參數**:
  - 邊框半徑
  - 邊框顏色
  - 漸層角度
  - 漸層起始顏色
  - 漸層結束顏色

### 5. 📨 UI 請求 (UI Requests)
- **選擇器**: `.UiRequests .UiRequestContainer .UiRequest .UiRequestInner`
- **可自訂參數**:
  - 背景漸層
  - 邊框顏色
  - 邊框半徑
  - 陰影效果

### 6. 💨 光環條 (Aura Bar)
- **選擇器**: `.AuraBarWrapper .AuraBar`
- **可自訂參數**:
  - 背景顏色
  - 邊框顏色
  - 邊框寬度
  - 邊框半徑
  - 高度比例

### 7. ✨ 附魔台 (Enchanting Table)
- **選擇器**: `.EnchantingTable .EnchantingTableBody .EnchantingTableLeft .PossibleEnchantments`
- **可自訂參數**:
  - 背景顏色
  - 邊框顏色
  - 邊框半徑
  - 標題文字顏色

### 8. 🏗️ 原理圖 (Schematic)
- **選擇器**: `.SchematicListContainer, .SchematicThumbnail, .SchematicName`
- **可自訂參數**:
  - 背景漸層
  - 邊框顏色
  - 邊框半徑
  - 陰影效果

### 9. 🎮 自訂遊戲 (Custom Game)
- **選擇器**: `.CustomGameListContainer, .CustomGameListInner`
- **可自訂參數**:
  - 背景顏色
  - 邊框半徑
  - 內邊距
  - 邊框顏色

### 10. 🏆 排行榜 (Leaderboard)
- **選擇器**: `.LobbyLeaderboardMenu .LobbyLeaderboardContainer .LobbyLeaderboard`
- **可自訂參數**:
  - 背景漸層
  - 邊框半徑
  - 邊框顏色
  - 文字顏色

## 原有功能模組 (17個)

以下功能已在 index.html 中預先配置，現在更加完整：

1. 🎯 自訂準心 (Crosshair)
2. 💬 聊天室美化 (Chat)
3. ⚔️ 快捷欄與物品 (Hotbar)
4. ❤️ 血條樣式 (Health Bar)
5. 🏠 主選單背景 (Menu)
6. 📱 手機版按鈕 (Mobile)
7. 🔘 新按鈕 (New Button)
8. 🏠 主選單主題 (Main Menu Theme)
9. ⚙️ 設定選單主題 (Settings Theme)
10. 🔘 按鈕主題 (Button Theme)
11. 👥 社交欄主題 (Social Bar Theme)
12. 📝 輸入框主題 (Input Theme)
13. 🎒 背包主題 (Inventory Theme)
14. 🛒 商店主題 (Shop Theme)
15. 👤 角色自訂主題 (Character Theme)
16. ⏳ 載入器主題 (Loader Theme)
17. 🎮 遊戲內標題主題 (In-Game Header Theme)

## 總計

- **總功能模組數**: 27個
- **新增模組數**: 10個
- **可自訂參數**: 100+

## 使用方式

1. 打開 `index.html` 在瀏覽器中
2. 從下拉選單選擇要自訂的功能模組
3. 點擊 "新增功能" 按鈕
4. 在生成的卡片中調整各項參數
5. CSS 代碼將即時更新在右側預覽框
6. 點擊 "複製 CSS" 按鈕將生成的 CSS 複製到剪貼板

## 參數類型說明

- **色彩選擇器** (Color): 點擊選擇顏色
- **文字輸入** (Text): 輸入網址或自訂值
- **數字輸入** (Number): 調整數值參數
- **滑動條** (Range): 拖動調整值域範圍

## 從 texture.css 提取的類別選擇器

本工具涵蓋了 texture.css 中的主要視覺元素，包括：
- 菜單和界面組件
- 按鈕和交互元素
- 輸入框和表單
- 遊戲內 UI 元素
- 動畫和特效容器
- 社交和排行榜功能
