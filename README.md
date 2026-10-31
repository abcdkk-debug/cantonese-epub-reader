# 粵讀 EPUB (Cantonese EPUB Audiobook Reader)

一個專為廣東話 (zh-HK) 朗讀優化的 iOS 風格 PWA (Progressive Web Application) 電子書閱讀器。支援離線閱讀、本地 EPUB 檔案解析、即時文字高亮以及流暢的廣東話語音合成 (TTS)。

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![PWA Ready](https://img.shields.io/badge/PWA-Ready-success.svg)
![Language](https://img.shields.io/badge/Language-Cantonese%20(zh--HK)-orange.svg)

---

## 🌟 主要功能 (Key Features)

- **原生 iOS 視覺設計**：採用 iOS SF 經典設計語言、毛玻璃（Glassmorphism）導航列及適應深色模式 (Dark Mode)。
- **純正廣東話朗讀 (zh-HK TTS)**：自動偵測並調用系統最佳廣東話語音引擎（如 iOS Sin-Ji / 善兒）。
- **同步文字高亮**：朗讀時自動高亮當前段落，並滾動至對應內容。
- **完整的播放控制**：支援播放/暫停、上下段落跳轉、多倍速調整 (0.75x – 2.0x) 及聲調 (Pitch) 微調。
- **PWA 離線支援**：內置 Service Worker 與 Web App Manifest，可將網頁直接「加入主畫面」，無網路亦可離線閱讀與朗讀。
- **純前端本地解析**：所有 EPUB 檔案均在瀏覽器內（透過 JSZip）完成解析，保護個人閱讀隱私，無需上傳至伺服器。

---

## 📱 安裝至 iPhone / iPad 主畫面

1. 使用 **Safari 瀏覽器** 開啟本項目的網址。
2. 點擊 Safari 底部的 **「分享」按鈕**（帶有向上箭頭的正方形圖示）。
3. 向下滾動並選擇 **「加入至主畫面」 (Add to Home Screen)**。
4. 點擊右上角的 **「新增」**，即可在主畫面生成 App 圖示，體驗全螢幕無邊框的 Web App。

---

## 🔒 鎖屏/背景模式播放建議 (iOS Safari 限制說明)

由於 iOS Safari 對於網頁版 Web Speech API (`speechSynthesis`) 有嚴格的系統限制（鎖屏或切換 App 後瀏覽器會自動暫停語音合成），若希望在 **iPhone 鎖屏後繼續收聽**，建議配合 iOS 內置的「朗讀螢幕」功能：

1. 開啟 iPhone **「設定」➔「輔助使用」➔「語音內容」**。
2. 開啟 **「朗讀螢幕」** 及 **「語音控制器」**。
3. 在語音清單中點選 **廣東話 (Cantonese)**，下載 **「Sin-Ji (增強版 / Premium)」** 以獲得最自然的真人語調。
4. 打開本 App 開啟章節後，**雙指從螢幕頂部向下滑動**，即可啟用系統級鎖屏播放。

---

## 🛠️ 技術棧 (Tech Stack)

- **HTML5 / CSS3 / JavaScript (ES6+)**
- **Tailwind CSS**：iOS UI 樣式與響應式排版
- **JSZip**：本地解析 EPUB 解壓縮與 XML/HTML 解析
- **Web Speech API**：廣東話 (`zh-HK`) 語音合成控制
- **Lucide Icons**：現代化圖示庫
- **Service Worker & Dynamic Manifest**：PWA 離線快取

---

## 🚀 部署指南 (Deployment)

### 使用 GitHub Pages 免費託管

1. Fork 或 Clone 本專案至你的 GitHub 帳號。
2. 確保主網頁檔案命名為 `index.html` 並位於專案根目錄。
3. 進入 GitHub 專案頁面 ➔ **Settings** ➔ **Pages**。
4. 在 **Source** 選擇 `main` (或 `master`) 分支與 `/ (root)` 資料夾，點擊 **Save**。
5. 等待 1-2 分鐘後，即可透過 GitHub 提供之 HTTPS 連結存取專案。

---

## 📄 開源許可 (License)

本專案採用 [MIT License](LICENSE) 開源授權。