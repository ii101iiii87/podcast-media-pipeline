# Podcast Media Pipeline

這是一個只有 Skills、不綁特定帳號或付費服務的 Codex Plugin。它把單集 Podcast 的製作流程整理成：音訊製作與檢查 → 創作者完整試聽核准 → 長影片與短影片 → 媒體 QA → 上傳計畫預覽 → 核准後排程發布 → 線上結果驗證。

最重要的硬性規則有兩個：

1. 使用者沒有明確確認「已聽完並接受匯出的 Podcast master」以前，不能開始製作長影片或短影片。
2. 沒有先讓使用者核准每個平台的檔案、標題、描述、縮圖、可見度、日期、時間與時區以前，不能上傳或排程。

## 安裝

公開到 GitHub 後：

```bash
codex plugin marketplace add ii101iiii87/podcast-media-pipeline --ref main
codex plugin add podcast-media-pipeline@podcast-media-tools
```

重新啟動 ChatGPT 桌面版、建立新的 Codex 任務，然後使用：

```text
使用 $podcast-media-pipeline:produce-and-publish 製作這一集 Podcast。
```

每個專案都可以把範例設定檔複製成 `podcast-pipeline.yaml`，寫入自己的品牌、音訊、長短影片與發布標準。請勿把密碼、Cookie、Token 或 MFA 備援碼寫入設定檔。

完整英文說明請見 [README.md](README.md)。
