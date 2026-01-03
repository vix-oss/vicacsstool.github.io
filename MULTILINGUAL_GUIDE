# 多語言支持說明

## 功能概述

index.html 現已支持多語言切換，用戶可以實時選擇喜歡的語言而無需重新加載頁面。

## 支持的語言

- 🇹🇼 **繁體中文** (Traditional Chinese) - `zh-TW` (默認)
- 🇨🇳 **簡體中文** (Simplified Chinese) - `zh-CN`
- 🇬🇧 **英文** (English) - `en`
- 🇯🇵 **日文** (日本語) - `ja`
- 🇰🇷 **韓文** (한국어) - `ko`

## 實現方式

### 1. 語言選擇器
位於頁面右上角，使用固定定位 (`position: fixed`)
- 用戶可以隨時點擊下拉菜單切換語言
- 選擇的語言會自動保存到瀏覽器的 LocalStorage

### 2. 翻譯系統
- 使用 `TRANSLATIONS` 對象存儲所有語言的文本
- 每個語言都有完整的鍵值對應關係
- 支持文本包括：
  - 界面標題和標籤
  - 按鈕文本
  - 錯誤提示信息

### 3. 語言切換函數

```javascript
// 翻譯函數 - 根據當前語言返回對應文本
function t(key) {
    return TRANSLATIONS[currentLanguage][key] || TRANSLATIONS['zh-TW'][key];
}

// 更新頁面所有文本
function updatePageLanguage() {
    // 更新 title, subtitle, labels, buttons 等
}

// 初始化語言（在頁面加載時調用）
function initLanguage() {
    // 載入保存的語言偏好設置或使用默認語言
}
```

### 4. 本地儲存
用戶選擇的語言會被保存到 `localStorage.preferredLanguage`
- 下次訪問時會自動恢復用戶的語言選擇

## 翻譯的文本鍵

| 鍵名 | 用途 |
|------|------|
| `language` | 語言標籤文本 |
| `title` | 頁面主標題 |
| `subtitle` | 頁面副標題 |
| `modules` | 功能模組標題 |
| `selectModule` | 選擇模組的標籤 |
| `selectOption` | 選擇框的 placeholder |
| `addBtn` | 添加功能按鈕 |
| `preview` | CSS 預覽區域標題 |
| `copyBtn` | 複製 CSS 按鈕 |
| `copySuccess` | 複製成功提示 |
| `emptyWarning` | 空值警告信息 |
| `removeBtn` | 移除按鈕 |
| `disabledMsg` | 禁用模組提示 |

## 添加新語言的步驟

若要添加新語言（例如俄文），按以下步驟：

### 1. 在 `TRANSLATIONS` 對象中添加新語言
```javascript
const TRANSLATIONS = {
    // ... 現有語言
    'ru': {
        'language': 'Язык:',
        'title': '🎨 Генератор CSS для Bloxd.io',
        'subtitle': 'Легко создавайте визуальные эффекты для своей игры',
        // ... 其他翻譯
    }
};
```

### 2. 在 HTML 的語言選擇器中添加選項
```html
<select id="languageSelect">
    <!-- ... 現有選項 -->
    <option value="ru">Русский (Russian)</option>
</select>
```

### 3. 確保所有鍵都被翻譯
每個新語言必須有 TRANSLATIONS 對象中定義的所有鍵。

## 技術細節

### CSS 樣式
語言選擇器使用以下樣式：
- 固定定位於右上角
- 深色背景，與頁面整體風格協調
- 懸停和聚焦時有視覺反饋
- 移動設備上響應式縮放

### JavaScript 事件
```javascript
// 監聽語言選擇器的變化
document.getElementById('languageSelect')
    .addEventListener('change', function(e) {
        currentLanguage = e.target.value;
        localStorage.setItem('preferredLanguage', currentLanguage);
        updatePageLanguage();
    });
```

### 兼容性
- 支持所有現代瀏覽器（Chrome, Firefox, Safari, Edge）
- 使用原生 JavaScript，無需額外庫
- 使用 LocalStorage API 存儲用戶偏好設置

## 使用示例

1. **訪問頁面**
   - 頁面會自動載入用戶之前選擇的語言，或默認使用繁體中文

2. **切換語言**
   - 點擊右上角的語言選擇器
   - 選擇所需的語言
   - 整個頁面的文本會立即更新

3. **語言偏好設置會被保存**
   - 下次訪問時會自動恢復

## 代碼結構

```
index.html
├── HTML 結構
│   ├── 語言選擇器 (頂部固定)
│   ├── 主容器
│   └── 功能面板
├── CSS 樣式
│   ├── 語言選擇器樣式
│   └── 響應式設計
└── JavaScript
    ├── TRANSLATIONS 翻譯對象 (5 種語言)
    ├── 語言控制函數
    │   ├── t(key) - 翻譯函數
    │   ├── updatePageLanguage() - 更新頁面
    │   └── initLanguage() - 初始化
    └── 事件監聽器
```

## 性能考量

- 翻譯數據在內存中緩存，切換語言時無需加載外部文件
- 使用原生 DOM 操作，性能高效
- LocalStorage 提供快速的持久化存儲

## 未來擴展建議

1. **動態加載翻譯** - 從外部 JSON 文件加載翻譯
2. **自動語言偵測** - 根據瀏覽器語言設置自動選擇
3. **更多語言支持** - 添加其他語言（俄文、西班牙文等）
4. **翻譯管理系統** - 集成翻譯工具以簡化維護
