# 專案：LINE 打卡

## 專案總覽

這是一個使用 LINE Front-end Framework (LIFF) 的自動打卡網頁應用程式。它會獲取使用者目前的位置，計算與預設地點的距離，然後傳送打卡狀態訊息（成功或失敗）到 LINE 聊天室。核心邏輯都包含在單一個 `index.html` 檔案中。

## 建置與執行

這是一個靜態網頁。要「執行」它，您需要透過 HTTPS 提供 `index.html` 檔案，這是 LIFF 的 `liff.getCurrentPosition()` 功能所要求的。一個簡單的方法是使用像 `ngrok` 這樣的工具，或將其部署到像 GitHub Pages 這樣的靜態網站託管服務。

1.  在本地端提供 `index.html` 檔案（例如，使用 `python -m http.server`）。
2.  使用像 `ngrok` 這樣的工具將本地伺服器公開到網際網路。
3.  在 LINE Developers console 中，將 LIFF 應用程式的端點 URL 更新為 `ngrok` 的 HTTPS URL。

## 開發慣例

此專案由單一的 HTML 檔案和嵌入的 JavaScript 組成。程式碼是自包含的，除了 LIFF SDK 之外沒有外部依賴。JavaScript 程式碼使用 Haversine 公式来計算兩個地理點之間的距離。
