# GitHub Pages 使用說明｜緊急求救訊號 AR

## 最重要的上傳方式

請把這個資料夾「裡面的所有檔案」放在 GitHub Pages 的根目錄。

正確的 repo 根目錄應該長這樣：

```text
index.html
preview_no_camera.html
diagnostics.html
test.html
.nojekyll
assets/
targets/
tools/
ar_timeline.json
README_使用方式.md
```

不要變成這樣：

```text
first_ar_card_emergency_signal_webar_github_ready/
  index.html
  assets/
  targets/
```

如果你把整個資料夾當成子資料夾上傳，那網址要改成：

```text
https://你的帳號.github.io/你的repo/first_ar_card_emergency_signal_webar_github_ready/index.html
```

## 依序測試這三個網址

假設 repo 網址是：

```text
https://你的帳號.github.io/你的repo/
```

請依序開：

1. `https://你的帳號.github.io/你的repo/test.html`
2. `https://你的帳號.github.io/你的repo/diagnostics.html`
3. `https://你的帳號.github.io/你的repo/preview_no_camera.html`
4. `https://你的帳號.github.io/你的repo/index.html`

## 最常見錯誤

### 1. GitHub Pages 只看到空白

通常是 `index.html` 不在 Pages 根目錄，或 CDN 沒載入。請先開 `diagnostics.html`。

### 2. diagnostics 顯示 `targets/first-card.mind` 404

代表你還沒有產生或上傳辨識檔。請打開：

```text
tools/generate-target.html
```

選：

```text
assets/target_card_front.png
```

產生 `first-card.mind`，然後放到：

```text
targets/first-card.mind
```

再 commit/push 到 GitHub。

### 3. preview_no_camera.html 可以看，但 index.html 不行

代表素材沒問題，多半是：
- `first-card.mind` 缺失
- 相機權限沒有允許
- CDN 被擋
- 手機瀏覽器不支援或沒有使用 HTTPS

### 4. test.html 都看不到

代表 GitHub Pages 沒有部署成功，或網址錯了。
