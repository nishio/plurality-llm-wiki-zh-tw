# plurality-llm-wiki-zh-tw

## 主題
**繁體中文（台灣）的多元宇宙論述**之概念體系。資料來源包括 Glen Weyl 與 Audrey Tang 的原文中文寫作、PDIS 出版物、台灣社群討論、Plurality 一書中文版（如有）等。

多語 [plurality-llm-wiki](https://github.com/nishio/plurality-llm-wiki) wiki 森林的一部分。本 wiki 是**自主的**，其頁面不必是 en wiki（[plurality-llm-wiki-en](https://github.com/nishio/plurality-llm-wiki-en)）或 ja wiki（[plurality-llm-wiki-ja](https://github.com/nishio/plurality-llm-wiki-ja)）的翻譯，也不必有對應。

> 各語言以不同方式分節（articulate）概念空間。差異本身即為本 wiki 森林的觀察與分析對象 ── 差異產生價值。

特別地，由於 [[words-as-public-goods-lt]]（parent wiki）所述「漢字作為兩種語言之間的道路」之觀察，本 zh-tw wiki 與 ja wiki 之間預期會有比與 en wiki 更密集的概念對應。這個假設將透過本 wiki 的實際運作來檢驗。

## 目錄結構

```
plurality-llm-wiki-zh-tw/
├── CLAUDE.md                          # 本檔案
├── raw/                               # 原始來源（gitignored）
├── wiki/
│   ├── index.md                       # 人類導覽（curated）
│   ├── index.txt                      # AI 完整目錄（auto-generated）
│   ├── log.md                         # 人類用近 7 日紀錄（full detail）
│   ├── log.txt                        # AI 用全部 compact 履歷（auto-generated）
│   ├── concepts/                      # 概念頁
│   ├── entities/                      # 人物・工具・專案
│   ├── sources/                       # 來源摘要
│   └── analyses/                      # 由問題衍生的分析
├── scripts/
│   ├── lint_wiki.py                   # wiki 健康檢查
│   ├── build_index_txt.py             # 從 frontmatter regenerate index.txt
│   └── refresh_logs.py                # 同步 log.txt 與 log.md（近 7 日）
```

## 語言間對應

語言間的概念對應記錄在 parent 的 [correspondences.yaml](https://github.com/nishio/plurality-llm-wiki/blob/main/correspondences.yaml)。等同於 Wikipedia 的 interlanguage link ── 一個列只主張「相同/相關的話題」，不主張內容對等。

新增 concept 頁面後：
- 在 `correspondences.yaml` 加入或擴充列，將其與 en / ja 對應概念連結（任一邊可為 null = 無對應）
- 或明確記錄為「無對應」（en: ~ / ja: ~）── 這不是疏漏而是觀察到的事實

## 頁面規則

### 共通
- 頁首加 YAML frontmatter：`type`, `summary`, `sources`
- 出處用 `[[來源頁名]]より` 或對應的中文表達標明
- 矛盾或未解決的論點寫在 `## Open Questions`
- 更新不要覆蓋既有內容，用 `## Updates` 追加
- wikilink 用 `[[頁面名]]`（Wikipedia 雙方括號形式）

### frontmatter 範例
```yaml
---
type: concept
summary: 一句話說明
sources:
  - 來源頁名.md
---
```

## 操作

### Index 維護（AI/人類分離，kouchou pattern）

- **`wiki/index.md`** — 人類用 curated nav。手動編輯
- **`wiki/index.txt`** — AI 用完整目錄。**不要手動編輯**。新增/重命名/刪除頁面或修改 frontmatter summary 後 regenerate：
  ```sh
  python3 scripts/build_index_txt.py
  ```

### Log 維護（AI/人類分離，kouchou pattern）

- **`wiki/log.md`** — 人類用近 7 日 full detail，newest first。手動在開頭加 `## [YYYY-MM-DD HH:MM] <type> | <title>`
- **`wiki/log.txt`** — AI 用全部 compact 履歷。**不要手動編輯**。在 log.md 加入新項目後 regenerate：
  ```sh
  python3 scripts/refresh_logs.py
  ```

### Ingest（raw → wiki）
1. 讀 `raw/` 內的新檔案
2. 對照既有 wiki 頁
3. 更新或新建（frontmatter 必須）
4. 頁面集合變動後執行 `python3 scripts/build_index_txt.py`
5. 在 log.md 開頭加 `## [YYYY-MM-DD HH:MM] ingest | <description>`
6. 執行 `python3 scripts/refresh_logs.py`
7. 若新概念可能與 en / ja 對應，更新 parent 的 `correspondences.yaml`

### Query
1. 搜尋 `wiki/` 回答
2. 有用的回答 filing back 到 `analyses/`
3. 在 log 記錄為 `filing-back` 並執行 `refresh_logs.py`

### Lint
1. 機械式：`python3 scripts/lint_wiki.py`
2. 語意式：矛盾、stale claim、概念頁缺漏、新問題的提案
3. 只在有檢出時記錄 lint log（無檢出由 `refresh_logs.py` 自動丟掉）

## 運作方針

- 來源是「參考」不是無批判採用
- 不強制與 en / ja 之間翻譯一致 ── 差異才是本 wiki 森林的主題
- schema（本檔）也透過實驗逐步改進
