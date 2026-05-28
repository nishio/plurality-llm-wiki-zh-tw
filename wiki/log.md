# Log

> 直近 7 日分のみ。全件 compact 履歴は [log.txt](log.txt)、それより古い entry の詳細は `git log -- wiki/log.md` で参照。
> 更新は `python3 scripts/refresh_logs.py` で log.txt と log.md を再生成する。

## [2026-05-28 21:30] ingest | 第三輪: pending pages 解消 (Section 4 章 + foil 概念 + Section 5 メカニズム + JA 起源概念)


parent `correspondences.yaml` zh-tw 列の pending references 26 件 → 0 件に解消する目的で、本書中文版 + 上游 manuscript の既存材料を元に 22 件の新 concept page を作成。

### 新規 concept pages (22 件)

**Section 4 章 (book chapter concept)**:
- [[結社與多元公眾]] (4-2 章 concept page)
- [[商業與信任]] (4-3 章 concept page)
- [[財產與契約]] (4-4 章 concept page)

**Foil 概念 (Plurality 反対路線)**:
- [[技術專家治理]] (Technocracy / 専家統治)
- [[技術官僚]] (Technocrat, ja-zh-tw 共通の role-noun split)
- [[自由意志主義]] (Libertarianism / 放任主義)
- [[自由意志主義者]] (Libertarian, 同様 role-noun split)
- [[一元原子論]] (Monist Atomism, 失敗路線の共通基盤)
- [[狹窄走廊]] (Narrow Corridor, Acemoglu & Robinson)

**Section 5 機制章**:
- [[後符號溝通]] (後符號交流 の譯語變體, parent registry 採用語)
- [[沉浸式共享現實]] (沉浸式共享實境 の譯語變體, parent registry 採用語)
- [[創意協作]] (5-3 章)

**AI / Policy concepts**:
- [[通用人工智慧]] (AGI)
- [[無條件基本收入]] (UBI)
- [[網路國家]] (Network State)
- [[預測式治理]] (Futarchy)
- [[⿻管理協定]] (Plural Management Protocol)
- [[去中心化自治組織]] (DAO)
- [[超模性]] (Supermodularity)

**漢字 bridge concepts (zh-tw / ja 共有)**:
- [[中央集權]] · [[反社會]] · [[國家]] · [[資本主義]]

**JA 起源 (鈴木健の系譜)**:
- [[分人]] · [[分人民主主義]] · [[PICSY]]

### 興味深い発見

1. **譯語並用の発見**: 後符號交流 vs 後符號溝通, 沉浸式共享實境 vs 沉浸式共享現實 — book manuscript と parent registry で異なる譯語を採用しており、両方を保持することで「翻譯實踐の人工物」として記録した。zh-tw 翻譯傳統がまだ標準化していない領域の証拠。
2. **役職名 / ideology split が ja-zh-tw 共通**: 技術專家治理 / 技術官僚 と 自由意志主義 / 自由意志主義者 は二語で分けるのが ja と zh-tw で共通する慣行。EN 側は ideology のみ page 化。これは「漢字圏特有の concept-role 分離 pattern」として記録すべき差異。
3. **漢字 bridge の continuum**: 字形完全一致 (資本主義) → 一文字差 (中央集権↔中央集權, 国家↔國家, 反社会↔反社會) → 字形差なく異字 (數位 ja-zh tw 完全一致) など、ja-zh-tw 漢字 bridge には gradient 構造があることが具体的に確認できた。

### parent 側との関係

parent `correspondences.yaml` の zh-tw 列 pending references 26 件 → **0 件**に解消。
全 registry annotation が child-wiki page に対応する状態を達成。

## [2026-05-28 17:30] ingest | 第二輪 ingest: GitHub API workaround で繁體中文資源取得




並列 JA / EN subagent と同様の `gh api` workaround によって, 前回 subagent が諦めた領域を実際に探索。多くの主要資源が GitHub 経由でアクセス可能と確認。

### 取得した raw 資料 (38 ファイル)

1. **pluralitybook/plurality 繁體中文 manuscript** (21 章): 第一輪未取得分の章節原稿を upstream GitHub から直接取得 ([[多元宇宙一書上游手稿]])。
2. **audreyt/civic.ai** (12 ファイル): [[仁工智慧計畫]] (Civic AI · 關懷六力) の繁體中文 tw-*.md 全集核心部分。Caroline Green と[[唐鳳]] が 2025-2026 牛津 AI 倫理研究院で発展させた framework。
3. **g0v/g0v.tw** (3 ファイル): [[g0v宣言]]、about、faq の公式繁體中文文書。
4. **PDIS/web-jekyll** (11 ファイル): [[唐鳳PDIS專欄]] 2022-2024 の代表的記事。

### 新規ページ

- **source (9)**: [[多元宇宙一書上游手稿]] [[結社與多元公眾章]] [[後符號交流章]] [[媒體章]] [[環境章]] [[商業與信任章]] [[仁工智慧計畫]] [[g0v宣言]] [[唐鳳PDIS專欄]]
- **concept (13)**:
  - 新通訊: [[後符號交流]] [[沉浸式共享實境]]
  - 自由與政策: [[結社自由]] [[多元公眾]] [[數位簽章]]
  - 機制設計: [[對齊大會]] [[我城對談]]
  - 仁工智慧: [[仁工智慧]] [[地神]] [[關懷六力]] と 6 力 ([[覺察力]] [[負責力]] [[勝任力]] [[回應力]] [[團結力]] [[共生力]])
- **entity (3)**: [[TAIDE]] [[Jaron-Lanier]] [[Tenzin-Yangtso]]
- **meta**: [[wishlist]]
- **既存頁更新 (3)**: [[g0v]] [[唐鳳]] [[數位公共基礎建設]]

### 最も興味深い発見 Top 3

1. **「仁工智慧」(Civic AI) という同音替字翻訳**: 「人工」→「仁」(儒家 benevolence) と置換。zh-tw 翻訳伝統中の「字義新生」戦略の先駆例。en の "civic" を「公民」「市民」と訳さず「仁」で表現することで, 概念が儒家倫理と直結。
2. **「窩心」翻訳問題と TAIDE モデル**: Llama 2 が「窩心」を nervous と誤訳, [[TAIDE]] は touched と正確。これは台湾標準語 (positive) vs 中国大陸用法 (negative) の語料差異の具体例で, 「文化主権」と AI 主権の本質的連結を示す。
3. **[[地神]] (Kami) の翻訳選択**: 日本神道「神 / カミ」を zh-tw が「神明」「土地公」「神祇」を避けて「地神」と訳す。「地」(local) を最大化する選択で, 仁工智慧の「在地、有界、可退場」設計原則と完全一致。

### 失敗源 (詳見 [[wishlist]])

7 candidate 群すべて GitHub access では不十分:
- PDIS sayit archive (機構直接 web 必要)
- 報導者 / 端傳媒 (paywall)
- 總統盃黑客松年次成果報告 (PDF only)
- 中央研究院学術論文 (paywall / PDF)
- g0v hackmd (非 GitHub platform)
- audreyt 個人 blog (確認待ち)
- 法律文書 (法規網站 only)

### parent 側との関係

新規概念 ([[仁工智慧]] [[地神]] [[關懷六力]] [[對齊大會]] 等) は en / ja 側にも対応がある可能性高い。次回 parent `correspondences.yaml` の update が必要。

## [2026-05-27 14:30] ingest | 第一輪 ingest: 繁體中文最新 Plurality 材料






從 [plurality.net/zh](https://www.plurality.net/zh/) 收集 18 份 raw 材料 (《[[多元宇宙一書中文版]]》各章節摘要)，ingest 為:

- **5 件 source**:
  - [[多元宇宙一書中文版]] (書本整體 overview)
  - [[數位觀照]] (1 序言)
  - [[玉山視野章]] (2-1)
  - [[數位民主的日常章]] (2-2)
  - [[我們遺忘的道章]] (3-3)

- **22 件 concept**:
  - 思想根源: [[數位]] [[失落之道]] [[連結社會]] [[控制論]] [[三民主義]] [[亨利·喬治]] [[太陽花運動]]
  - 機制設計: [[多元投票]] [[平方投票]] [[平方融資]] [[流動民主]] [[杜瓦傑法則]] [[擴增審議]] [[廣泛聆聽]] [[自適應行政]] [[社會市場]] [[生成式基礎模型]] [[數據聯盟]]
  - 自由與政策: [[身分與人格權]] [[近用]] [[政策]] [[數位公共基礎建設]] [[利害關係人企業]] [[協作技術與民主]]
  - 台灣脈絡: [[玉山視野]] [[數位民主]] [[總統盃黑客松]] [[監控資本主義]]

- **5 件 entity**: [[唐鳳]] [[衛谷倫]] [[g0v]] [[PDIS]] [[高嘉良]]

- **2 件既存頁更新**: [[多元]] と [[為何我是多元宇宙人]] に Updates section 追加。

### 主要發現

1. **「數位」 = digital + plural 的中文版獨有雙重意涵**: [[數位觀照]] 序言明示。⿻ 記號詞源根據。
2. **三民主義承接鏈**: [[亨利·喬治]] → 孫中山 [[三民主義]] (民生主義) → 中華民國憲法 → 今日台灣 [[社會市場]] 機制。本書 2-1 / 3-2 / 5-7 章一貫貫穿。
3. **「平方投票」是 ja→ 漢字 bridge 不通過的稀有例**: ja 採用 katakana loanword「クアドラティック投票」、zh 採漢字翻譯「[[平方投票]]」。

### parent 側との関係

parent `correspondences.yaml` の zh-tw 列の dangling reference を主に解消する向き。新規概念ページの追加で parent 側 update が必要かは別途 lint で確認。
