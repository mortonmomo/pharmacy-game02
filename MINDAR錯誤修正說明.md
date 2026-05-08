# generate-target.html 修正版說明

如果先前出現：

`MINDAR is not defined`

原因是 MindAR 編譯器外部 JS 沒有載入成功。這份修正版會自動嘗試兩個 CDN 來源，並明確顯示載入狀態。

## 使用方式

1. 打開 `tools/generate-target.html`
2. 等按鈕從「載入編譯器中……」變成「產生 first-card.mind」
3. 選 `assets/target_card_front.png`
4. 按「產生 first-card.mind」
5. 將下載的 `first-card.mind` 放進 `targets/`

若仍失敗，通常是網路或瀏覽器擋 CDN。請把整包先放到 GitHub Pages / Netlify 後，再從 HTTPS 頁面開啟 `tools/generate-target.html`。
