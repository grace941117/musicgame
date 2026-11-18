# 節奏法師・音樂廚房

上傳這個資料夾內的 `index.html` 與 `assets/`，讓 `index.html` 位於靜態主機的網站根目錄。若主機詢問輸出目錄，使用目前資料夾。開啟部署網址即可遊玩。

桌機使用鍵盤 J／K，手機使用遊戲畫面下方的觸控按鈕。場景由 Three.js 繪製，配樂與音效由瀏覽器即時產生。使用支援 WebGL 2 與 Web Audio 的瀏覽器。

## 檔案調整

| 原路徑 | 上傳版路徑 |
| --- | --- |
| `public/index.html` | `index.html` |
| 線上的 Three.js r128 相依檔 | `assets/three-min.js`，本地隨附 r170 |
| Three.js 授權 | `assets/three-license.txt` |

`index.html` 透過相對路徑 `assets/three-min.js` 載入引擎。遊戲沒有獨立的圖片或音效檔需要搬移。

## 上線後設定分享網址

在 index.html 的 <head> 找到分享網址註解。將 og:url 的 https://example.com/ 改成實際上線首頁完整網址，將 og:image 改成同一網站上 assets/share.png 的完整公開網址。若網站架在子目錄，兩個網址皆保留子目錄。移除包住這些標籤的註解符號與說明文字，再重新部署。用無痕視窗確認首頁與分享圖網址均能開啟。
