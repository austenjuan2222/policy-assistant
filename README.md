# 保單機器人

三商品保單查詢、條款來源與費率試算的完整專案快照。

## 下載與啟動

下載 `policy-assistant-complete.zip` 並完整解壓縮。ZIP 內包含程式、原始 PDF／Excel、知識資料、資料處理工具、測試和架構簡報。

安裝符合 `package.json` 要求的 Node.js（>=22.13）與 npm，進入 `policy-demo/site` 後執行：

```sh
npm ci
npm run dev
```

開啟終端機顯示的本機網址。知識 JSON 與公開 PDF 已附，啟動時無須重新整理資料。

## AI 設定

本包不含 API 金鑰。文件查詢和費率試算可以先使用。AI 問答需自行設定未追蹤的 `.env.local`，參照 ZIP 中 `lib/ai-config.mjs` 設定供應商、自己的金鑰與帳號目前可用的模型。

## 檔案與發布

- 根目錄：12 份原始保單與費率文件。
- `policy-demo/site/`：前端、後端 API、知識資料、公開 PDF、套件鎖檔與測試。
- `policy-demo/tools/`：來源擷取及資料整理工具。
- `policy-demo/data/`：擷取後的資料及目錄。
- `簡報/`：網站架構與 Sites 發布詳解。

保留必要的 `site/build/` 平台整合原始檔，排除重複舊部署產物、套件、暫存檔、Git 紀錄及秘密設定。

這是本機快照，不保證與最新線上部署相同。舊進度記錄應與現有程式及實測交叉核對。SCB 15 年期費率等缺件與專業內容仍需覆核。

既有 Sites 網站權限不隨下載移轉。新建 Site 時需申請自己的 project_id，不能直接使用原 `.openai/hosting.json` 的網站身分發布。

原始 Excel 可能含成本與隱藏工作表，請維持私人儲存庫並僅分享給可接手完整資料的人。
