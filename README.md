# 勞務報酬單產生器｜一璟室內裝修設計有限公司

自動試算扣繳稅額與二代健保補充保費，產出可簽章 A4 PDF，並可同步登錄到公司 Google 試算表。

- `index.html`：網頁（GitHub Pages）
- `apps-script/Code.gs`：後台程式（貼到 Google 試算表的 Apps Script）

## 後台設定
1. 新建 Google 試算表 → 擴充功能 → Apps Script，貼上 `Code.gs`
2. 執行 `setup`（首次需授權）
3. 部署 → 新增部署作業 → 類型「網頁應用程式」；執行身分「我」；誰可以存取「所有人」
4. 複製網頁應用程式網址，貼到 `index.html` 的 `BACKEND_URL = ''`，上傳到 GitHub

修改 Code.gs 後需「管理部署作業 → 編輯 → 版本：新版本」才會生效。
不需密碼；每分鐘最多登錄 10 筆（Code.gs 的 RATE_LIMIT）。

## 年度參數
修改 `index.html` 內 `RULES` 區塊。
