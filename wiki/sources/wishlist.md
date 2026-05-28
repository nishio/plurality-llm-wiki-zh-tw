---
type: source
summary: 嘗試取得但無法 access 的 source 列表。等待人類手動取得協助。
raw_sources:
  - wishlist
---

# Wishlist (需要人類取得協助)

本頁面記錄嘗試取得但無法 access 的 source。人類手動 fetch 後放入 raw/, 後續 ingest 即可取入。

## PDIS sayit archive

### https://sayit.archive.tw/ (推測 URL, 未驗證存在)

- **預期內容**: 唐鳳數位部長期間 (2022-2024) 所有對外發言、會議、訪談的逐字稿正典。是「**徹底透明**」原則的具體實踐, 也是繁體中文 Plurality 論述最權威的口語原典。
- **嘗試**: 2026-05-28 via gh api 搜尋 audreyt org `sayit-transcripts` 與 PDIS 相關 repo 未找到 sayit 鏡像
- **結果**: 未找到 GitHub mirror。實體 sayit 平台需直接 WebFetch
- **協助動作**: 人類在 sayit.archive.tw 或 https://sayit.pdis.nat.gov.tw 確認狀態, 如仍存活則匯出大量 transcripts (例如 2022 / 2023 / 2024 各取代表性 10 篇), 放入 raw/

## 報導者 / 端傳媒 系列 Plurality 報導

### https://www.twreporter.org/ (報導者)
- **預期內容**: 對唐鳳、g0v、台灣數位民主等議題的深度新聞報導。報導者作為**公益新聞媒體**, 文章品質高且立場獨立。
- **嘗試**: 2026-05-28 via WebFetch 未嘗試 (假設失敗為非 github 域)
- **結果**: 預期需 paywall / cookie / JS rendering, gh api 無法取得
- **協助動作**: 人類在 twreporter.org 搜尋「唐鳳」、「g0v」、「數位民主」、「多元宇宙」並取得 5-10 篇深度報導, 放入 raw/

### https://theinitium.com/ (端傳媒)
- **預期內容**: 端傳媒對唐鳳、台灣公民科技的中港台三地視角報導。香港停運後, 端的台灣相關內容仍是繁體中文圈重要視角。
- **嘗試**: 2026-05-28 via WebFetch 未嘗試
- **結果**: 預期 paywall
- **協助動作**: 人類取得相關文章後放入 raw/, 注意確認授權

## 總統盃黑客松年次成果報告

### https://presidential-hackathon.taiwan.gov.tw/ (官方網站)
- **預期內容**: 2018 起每年的總統盃黑客松卓越團隊與優勝團隊成果報告。是 Plurality 的「**[[平方投票]]在政府場域實踐**」的官方文件。
- **嘗試**: 2026-05-28 via gh api search 找到 `lu791019/2020-presidential-hackathon.taiwan.gov` 但只是某個團隊的個人提案, 非官方檔案
- **結果**: 政府官方網站可能有 PDF 報告但 gh api 無法取得; GitHub 上無 mirror
- **協助動作**: 人類從 https://presidential-hackathon.taiwan.gov.tw/ 下載 2018-2024 年度成果報告 PDF, 放入 raw/

## 中央研究院 學術論文 (Plurality 相關)

### 中研院政治所、社會所、人文社會中心
- **預期內容**: 中研院 (Academia Sinica) 對 Plurality / 數位民主 / 審議民主的中文學術論文。學術用詞與譯詞具有規範性。
- **嘗試**: 2026-05-28 via gh api search 未嘗試 (推測中研院 repos 不公開或不存在)
- **結果**: 學術論文一般以 PDF 形式在期刊網站, 非 GitHub
- **協助動作**: 人類在中研院 OpenHouse 或台灣期刊論文網 (例如 [華藝線上圖書館](https://www.airitilibrary.com/)) 搜尋相關論文, 取得 PDF 後放入 raw/

## g0v hackmd 大量會議記錄

### https://g0v.hackmd.io/
- **預期內容**: g0v 黑客松、社群活動的工作筆記、討論記錄、決議。重要實例: 2019 g0v 宣言修訂討論。
- **嘗試**: 2026-05-28 via gh api 無法存取 hackmd 內容
- **結果**: HackMD 內容不在 GitHub 上 (HackMD 為獨立平台)
- **協助動作**: 人類匯出特定重要會議記錄為 markdown, 放入 raw/

## audreyt sayit / blog 全集

### https://audreyt.org/
- **預期內容**: 唐鳳個人網站, 包含演講、寫作、訪談的中英文記錄。
- **嘗試**: 2026-05-28 via gh api 未確認 audreyt/audreyt 是否有 mirror
- **結果**: 待確認
- **協助動作**: 人類確認後協助匯入

## 跨語言對應參考: 「對齊大會」/「我城對談」的法律文書

### 台灣《證券投資信託及顧問法》修正案 (2023)
- **預期內容**: 對齊大會結論被法制化的證據文件。
- **嘗試**: 2026-05-28 未嘗試 (政府法規網站)
- **結果**: 待確認
- **協助動作**: 人類從全國法規資料庫取得相關修正條文與立法理由書, 放入 raw/

## 第二輪 ingest 的結果摘要

### 成功取得 (透過 `gh api`)
- pluralitybook/plurality 繁體中文 manuscript: 21 章 (補上第一輪未取的 0/3-0/3-1/4-0/4-2/4-3/4-4/4-5/5-1/5-2/5-3/6-1/6-2/6-3/6-4/6-5/8)
- audreyt/civic.ai: 12 個 tw-*.md 檔 (manifesto + faq + 6 力 + 4 篇核心論文)
- g0v/g0v.tw: 官方宣言、about、faq
- PDIS/web-jekyll: 11 篇唐鳳 PDIS 專欄

### 無法取得 / 等待協助
- 上述 7 個 candidate 群皆需要人類協助 (paywall / 非 GitHub 平台 / PDF 形式 / 機構網站)
