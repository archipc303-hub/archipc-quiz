# archipc-quiz
由 EZPage 建立的網站 - Deployed by EZPage
💻 ARCHI PC 核心診斷測驗 (Diagnostic Quiz)

這是一個專為 ARCHI PC 打造的互動式網頁測驗系統。透過情境式問答，分析使用者的「效能 (Performance)」、「穩定 (Stability)」與「美學 (Aesthetics)」需求，最終將使用者歸類為 12 種專屬科技人格之一，並無縫引導至官方 LINE 或 Instagram 進行客製化主機報價。

✨ 核心特色

🚀 零編譯部署 (Zero-Build)：採用純粹的 HTML + CDN 引入 React 與 Tailwind CSS，無需 Node.js 或 Webpack 打包，只要有瀏覽器就能跑，完美適配 GitHub Pages。

🧠 動態計分引擎：後台隱藏 P/S/A 三軸計分系統，根據玩家選擇精準推算硬體痛點。

📸 社交擴散功能 (Viral Sharing)：內建 html2canvas 引擎，一鍵自動擷取結果圖卡並下載至設備，同時將通關密語複製到剪貼簿。

🤖 智慧客服導流：自動生成專屬「診斷代碼 (SysCode)」與「取件碼 (TicketID)」，並一鍵跳轉至 ARCHI PC 的官方 LINE / IG 聊天室。

📁 檔案結構與部署方式

本專案結構極度輕量，請確保您的 GitHub 儲存庫（或網頁伺服器）包含以下結構：

archipc-quiz/
 ├── index.html       # 核心主程式 (包含所有邏輯與樣式)
 └── images/          # ⚠️ 必須建立此資料夾，並放入以下 12 張對應的 JPG 圖片
      ├── x-dev.jpg    (全能極客)
      ├── d-elite.jpg  (數據菁英)
      ├── m-max.jpg    (影音巨匠)
      ├── c-pro.jpg    (專業創作者)
      ├── b-pro.jpg    (企業領袖)
      ├── s-star.jpg   (魅影實況主)
      ├── p-ult.jpg    (效能硬核玩家)
      ├── t-pop.jpg    (潮流玩家)
      ├── v-max.jpg    (桌面美學大師)
      ├── g-cas.jpg    (休閒電玩咖)
      ├── w-lite.jpg   (數位游牧者)
      └── e-opt.jpg    (務實精算師)


🚀 如何部署 (GitHub Pages)

將 index.html 以及包含圖片的 images/ 資料夾上傳至您的 GitHub 儲存庫。

進入該儲存庫的 Settings -> Pages。

在 Build and deployment 中，將 Source 設定為 Deploy from a branch。

Branch 選擇 main (或您上傳的分支)，資料夾選擇 /(root)，點擊 Save。

等待約 1~2 分鐘，您的測驗網站即可上線！

🛠️ 客製化與修改指南

1. 修改官方客服連結

如果您未來更換了 LINE 或 IG 帳號，請用文字編輯器打開 index.html，大約在第 197 行附近，找到以下區塊並修改網址即可：

// 👇 ⚠️ 聯絡網址設定區 ⚠️ 👇
const LINE_LINK = "[https://page.line.me/127ikpql](https://page.line.me/127ikpql)"; // LINE 官方主頁連結
const IG_LINK = "[https://ig.me/m/archi.pc_official](https://ig.me/m/archi.pc_official)"; // IG 私訊連結
// 👆 ======================= 👆


2. 新增或修改題目

請在 index.html 內搜尋 const quizFlow = {，您可以在此區塊中自由更改題目 (title)、選項 (text)、跳轉邏輯 (next) 以及對應的權重加分 (effects)。

Created for ARCHI PC. Powered by React & Tailwind CSS.
