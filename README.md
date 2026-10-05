# 📸 PhotoCool - 高效能本地照片去重與相似分類工具

[![Latest Release](https://img.shields.io/github/v/release/Su3TvT/photocool-Rust-?label=Download%20PhotoCool.exe&color=brightgreen)]([https://github.com/Su3TvT/photocool-Rust-/releases/latest](https://github.com/Su3TvT/photocool-Rust-/releases/tag/%E5%84%AA%E5%8C%96%E6%80%A7%E8%83%BD))
[![Platform](https://img.shields.io/badge/Platform-Windows%20x64-blue.svg)](https://github.com/Su3TvT/photocool-Rust-/releases)

> **[Note / 說明]** 
> 本專案目前僅提供 Windows 預編譯版本（`.exe` 發布檔），源碼暫不開源。
> This repository currently hosts pre-compiled binaries (`.exe`) for Windows only. Source code is closed-source for now.

---

## 📥 最新版本下載 (Download)

👉 **[點此前往 Releases 頁面下載最新版 PhotoCool.exe](https://github.com/Su3TvT/photocool-Rust-/releases/latest)**

---

## 🌟 軟體簡介 (Overview)

**PhotoCool** 是一款基於 Rust 構建的高效能本地照片比對與自動分類工具。專為擁有龐大相冊、需要快速清理完全重複與相似照片的使用者設計。

不論是完全相同的檔案，還是經過壓縮、裁剪、微調光影甚至水平翻轉的相似圖片，PhotoCool 都能在**完全不安裝額外依賴**的情況下，於本地端快速完成比對與歸類。

---

## 🔥 核心功能亮點 (Key Features)

- **⚡ 極速兩階段比對 (Two-Stage Matching)**
  - **階段 1 (完全重複)**：基於 SHA-256 高速哈希，秒級找出內容完全一致的重複照片。
  - **階段 2 (視覺相似)**：採用 Gradient pHash 算法 + 128x128/32x32 雙階縮放與 8-bit 高覆蓋率分桶，準確辨識相似照片（含鏡像翻轉）。
- **🛡️ 超強穩定性與相容性 (Robust Engine)**
  - 內建 Alpha 圖層白底壓平機制，完美支援 PNG / WebP 透明圖層比對。
  - 全流程 Panic 防護與安全多執行緒池，大相冊掃描不閃退。
- **📂 智慧資料夾歸類與無損還原 (Smart Move & Regex Undo)**
  - 自動生成 `Exact_photos` 與 `Similar_photos` 分類資料夾，附帶同名防覆蓋機制。
  - **免 JSON 無損還原引擎**：隨時執行 `--undo` 命令即可將檔名與位置還原至分類前狀態。
- **🌐 視覺化對照總覽 (HTML Summary)**
  - 分類完成後自動生成 `分類總覽.html`，以響應式卡片網頁呈現各組照片預覽與數量。

---

## 🚀 下一代前瞻 (Coming Soon)

> **🤖 AI 語意理解版即將登場！**
> 我們正在開發下一代版本，將正式接入 **ONNX Runtime AI 模型**！屆時除了傳統哈希比對外，還能透過深度學習 Embedding 實現「語意級相似度辨識」（例如：同場景不同角度、同人物不同表情等），敬請期待！

---

## 🛠️️ 使用說明 (Usage)

### 方式 1：雙擊直接執行
1. [下載最新發行的 `PhotoCool.exe`](https://github.com/Su3TvT/photocool-Rust-/releases/latest)。
2. 雙擊執行 `PhotoCool.exe`。
3. 輸入你的照片資料夾路徑（例如 `D:\Photos`）。
4. 選擇 `0` 開始進行分類，或選擇 `1` 執行檔案還原（Undo）。

### 方式 2：拖曳資料夾或命令列執行
- **資料夾拖曳**：直接將照片資料夾拖曳到 `PhotoCool.exe` 圖示上即可自動載入路徑。
- **命令行啟動**：
  ```cmd
  PhotoCool.exe "D:\Your\Photo\Path"


---
🔒 隱私與安全 (Privacy & Security)
100% 本地運算：所有特徵提取與檔案處理均在你的電腦本地完成，絕不上傳任何圖片或數據至雲端。

綠色免安裝：單一 .exe 檔，隨開即用，不寫入系統登錄檔。

📥 免責聲明 (Disclaimer)
本軟體為免費提供之預編譯工具，請在執行大規模檔案處理前自行備份重要照片。

軟體僅做檔案整理與位置移動，不會主動刪除你的原始照片檔案。
