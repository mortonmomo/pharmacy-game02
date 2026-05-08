# 第一段 AR 卡｜緊急求救訊號｜WebAR 原型包

這個資料夾是「可部署成 WebAR」的第一段 AR 卡原型。

## AR 動作

掃描 `assets/target_card_front.png` 後，會在卡片上疊出約 12 秒的 AR 分層動畫：

1. 警報紅燈閃
2. 史萊姆王 hologram 浮出
3. 求救訊息框出現
4. 健寶驚訝：「咦？這是……緊急求救訊號？」
5. 健寶回應：「撐著，我來了。」

## 檔案說明

- `index.html`：真正的 WebAR 頁面。
- `preview_no_camera.html`：不用相機的瀏覽器預覽。
- `assets/target_card_front.png`：實體卡正面，也是 image target。可列印或用平板螢幕顯示。
- `assets/*.png`：AR 疊加層素材。
- `tools/generate-target.html`：MindAR target 產生器。
- `targets/`：請放入產生出的 `first-card.mind`。
- `ar_timeline.json`：播放流程與素材對照。

## 使用步驟

### 1. 先看非 AR 預覽

用電腦瀏覽器打開：

`preview_no_camera.html`

這可以檢查分層動畫節奏，不需要相機。

### 2. 產生 MindAR target

打開：

`tools/generate-target.html`

選擇：

`assets/target_card_front.png`

按下「產生 first-card.mind」。

下載後，把 `first-card.mind` 放入：

`targets/first-card.mind`

### 3. 部署到 HTTPS 網頁空間

WebAR 相機通常需要 HTTPS。建議放到 GitHub Pages、Netlify、Vercel 或學校網頁空間。

部署後，用手機開啟：

`index.html`

允許相機，對準 `assets/target_card_front.png`，即可觸發 AR。

## 注意

- 如果只用 `file://` 直接開 `index.html`，手機相機通常不會正常啟動。
- 如果沒有 `targets/first-card.mind`，AR 頁面會無法辨識圖卡。
- 目前是第一版可用原型；正式製作時，可以把 PNG 素材換成美術完稿。
