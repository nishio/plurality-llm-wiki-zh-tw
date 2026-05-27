# plurality-llm-wiki-zh-tw

多語 [plurality-llm-wiki](https://github.com/nishio/plurality-llm-wiki) wiki 森林的**繁體中文（台灣）版**。繁體中文「多元宇宙」論述中的概念體系 ── 來源包括 Glen Weyl 與 Audrey Tang 的原文中文寫作、PDIS 出版物、Plurality 一書中文版、台灣社群討論等。

## 與兄弟 wiki 的關係

本 wiki **自主**。頁面不必是 [en 側 wiki](https://github.com/nishio/plurality-llm-wiki-en) 或 [ja 側 wiki](https://github.com/nishio/plurality-llm-wiki-ja) 的翻譯，也不必有對應。各語言以不同方式分節（articulate）概念空間，差異本身即為 parent wiki 森林的觀察與分析對象。

語言間對應（與明示性的缺漏）由 parent 的 [correspondences.yaml](https://github.com/nishio/plurality-llm-wiki/blob/main/correspondences.yaml) 追蹤。其中的列等同於 Wikipedia 的 interlanguage link ── 主張「這些頁面是同一/相關話題」，但不主張內容對等。

特別地，parent wiki 的觀察（[words-as-public-goods-lt](https://github.com/nishio/plurality-llm-wiki/blob/main/wiki/sources/words-as-public-goods-lt.md) / [kanji-as-ja-zh-bridge](https://github.com/nishio/plurality-llm-wiki/blob/main/wiki/analyses/kanji-as-ja-zh-bridge.md)）指出 ja-zh 之間透過漢字共享存在比 en-ja 更密集的對應路徑。本 wiki 的實際運作將檢驗這個假設。

## Repository 構成

```
wiki/
├── index.md             人類用 curated 導覽
├── log.md               人類用近 7 日 activity log
├── concepts/            概念頁
├── entities/            人物・工具・專案
├── sources/             來源摘要
└── analyses/            由問題衍生的分析
```

`index.txt` / `log.txt` 為 AI 用 auto-generated 檔案 ── 不要手動編輯。

## Contributor

- 運作細節、頁面規約、frontmatter schema：[CLAUDE.md](CLAUDE.md)
- 頁面新增・rename・刪除後：`python3 scripts/build_index_txt.py`
- log 追加後：`python3 scripts/refresh_logs.py`
- 機械式健全檢查：`python3 scripts/lint_wiki.py`

## 運作方針

- 來源是「參考」不是無批判採用
- 不強制與 en / ja 之間翻譯一致 ── 差異才是本 wiki 森林的主題
- schema（CLAUDE.md）也透過實驗逐步改進
