# 節奏法師・音樂廚房｜GitHub 與 Vercel 上架

## 一、把網站放上 GitHub

1. 在 https://github.com/new 建立儲存庫。名稱可填 rhythm-mage，勾選 Add a README file，讓儲存庫建立後立即出現上傳選單。
2. 解開 ZIP，進入 rhythm-mage 資料夾。在 GitHub 儲存庫選 Add file → Upload files。
3. 拖入 index.html、vercel.json、整個 assets 資料夾及本說明。可保留 GitHub 自動建立的 README.md，ZIP 裡的 readme.md 可留在本機，避免只差大小寫的同名檔。
4. 點 Commit changes。確認儲存庫首頁能直接看見 index.html、vercel.json 和 assets 資料夾。

## 二、匯入 Vercel

1. 開啟 https://vercel.com/new ，登入並連接 GitHub，匯入剛建立的儲存庫。
2. Project Name 可填 rhythm-mage。若名稱被占用，改用其他名稱。
3. Root Directory 使用儲存庫根目錄（含 index.html 和 vercel.json）。網站採 Other，Build Command 留空，Output Directory 為「.」，無需安裝套件或設定環境變數。ZIP 內的 vercel.json 已指定靜態配置。
4. 點 Deploy。完成後從專案 Domains 或部署頁取得長期使用的正式網址。先確認正式網址可以開啟首頁。

## 三、啟用分享卡

用 GitHub 編輯 index.html。在開頭找到「部署後將下方的範例網域換成你的實際網域」的註解段落。

- og:url 改成實際首頁完整網址，例如 https://your-project.vercel.app/
- og:image 改成同一網址下的圖片，例如 https://your-project.vercel.app/assets/share.png
- 移除包住這幾個 meta 標籤的開頭註解行和結尾註解符號，保留 meta 標籤本身，再提交到 Vercel 的 Production Branch，通常是 main。
- 等 Vercel 完成新部署後，用無痕視窗確認首頁及 assets/share.png 都能正常開啟。

## 四、上線驗收

- 桌機開始任一關，確認廚房畫面和聲音正常，鍵盤 J／K 可操作。
- 手機點開始，確認畫面下方出現兩顆觸控鍵。
- 核對瀏覽器頁籤標題、小圖示及公開的分享圖片網址，並把正式首頁網址貼到要分享的平台。
- 如果首頁出現 404，檢查 Root Directory 和 GitHub 儲存庫根目錄下的 index.html。若 3D 無法載入，確認 assets/three-min.js 已與 index.html 一起上傳，且檔名大小寫正確。

官方文件

- https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository
- https://vercel.com/docs/git
- https://vercel.com/docs/builds/configure-a-build
