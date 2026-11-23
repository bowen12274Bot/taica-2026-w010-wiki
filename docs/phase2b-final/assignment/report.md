# 從來源回執到五章教材

## 本輪交付與查核附件

[本輪正式交付](../../../index.html) · [全文閱讀目錄](../../../slides/book/index.html#contents) · [106 項知識與閱讀段落對照](../../phase2b-publish/coverage.html)

[28 份回執總表](source-receipts.csv)列出三個階段的 28 份正式來源。本輪節錄其中 6 份公開來源的正式回執與讀回定位，並附查詢失敗、修正和複驗紀錄。每份節錄都能回查原檔行號、原檔與附件的 SHA-256。[歷史證據索引](raw-evidence/index.html) · [Markdown 證據索引](raw-evidence/index.md) · [中文來源與證據分類](raw-evidence/classification.html)

教師抽查可從 [歷史盲查第三題](raw-evidence/index.html#query) 開始。先讀原問句兩次零命中，再讀關鍵字命中後 T04 對兩筆固定資料的要求，最後開啟 [2.B.03 瀏覽器驗證：對照同一次操作的請求、回應與畫面](../../../slides/book/index.html#C19)，查看判斷題如何引用 T04。教材對照完成於本輪。

第十週作業｜《多 Agent 軟體開發實踐指南》教師核驗報告

2026-11-22 二次查讀。**三份歷史紀錄合計有 28 份不同來源的正式匯入回執**，其中 20 份為公開文件整理、8 份為私人研究或補充整理。教師可以在本頁查到每份來源的作者歸屬、寫入時間與讀回頁面。要評估教材是否忠於證據，可從第四章的「失聯能否重派」或第五章的「怎樣比較效率」直接查起。

<a id="scope"></a>

## 作業依據與可判定範圍

根目錄 `README.md` 稱本案為「第十週課程作業」；`docs/project-spec.md` 首段列出六項交付。`docs/workflow-plan.md` 說明初始階段的授權順序。查了主樹根目錄、初始資料包目錄及專案需求文件，找到的是專案對作業的轉述與研究資料，未辨識到教師簽發的原題或評分規準。因此下表按專案規格對照，原題措辭與配分待教師確認。

| 教師可查的作業要求 | 本頁可核對的材料 | 判讀範圍 |
|---|---|---|
| LLM Wiki 至少五份來源 | [28 份正式回執](#receipts)，另附 [CSV](source-receipts.csv) | 已驗證歷史寫入，預演另列 |
| 五章知識內容；HTML 教學簡報引用 Wiki | [五章抽查路徑](#chapters)，各舉一項教材判斷 | 已驗證歷史落點；四個審定互動原型只涵蓋其中四章 |
| 來源到簡報的 Loop／Graph | [節點、回返及停止條件](#graph) | 舊階段可追查；本輪關卡見上方正式交付紀錄 |
| 執行及內容檢查紀錄 | [成功與失敗的查讀](#query)、[修正案例](#repair) | 區分回執、內容支持、檢索失敗與編輯測試 |
| 教師可瀏覽成果 | 本頁、歷史附件與回執總表可離線開啟 | 上方本輪正式交付頁彙整全書驗收 |

<a id="timeline"></a>

## 從空 Wiki 到十四個細講位置

| 階段 | 實際觀察與工具 | 紀錄定位（專案相對路徑） |
|---|---|---|
| 0｜連線 | 2026-11-21 21:31:03 台北時間，新 Codex 程序經 stdio 對官方 Microsoft LLM Wiki bundle 呼叫 `wiki_status`、`wiki_list_sources`、`wiki_list_pages`。來源 0、知識頁 0；列檔僅原生 index、log。先前 npm 查詢回 E404。 | `evidence/codex-mcp-check.md`「執行順序」；`evidence/mcp-check.md`「套件與啟動入口」 |
| 1｜建庫 | 12 來源、14 概念、5 導覽。U-A／B／C 初次摘要有截斷，經 `wiki_update_page` 補全及 `wiki_read_page` 比對。 | `evidence/ingest-log.md` 表後說明；`evidence/phase1-report.md` |
| 1B｜補足知識缺口 | 加 13 來源，累計 25 來源、45 頁。P06 等工具文件和 S01 操作觀察整合於 tool-management；原 31 頁舊正文仍可讀。14 新題、3 反向歸屬、10 舊題均有查詢與讀頁；部分問句已進索引。 | `evidence/phase1b/final-report.md` B–E；`evidence/phase1b/query-validation.md` 新題 1–4 |
| 1C｜整理成可教的路徑 | 再加 3 來源，合計 62 內容頁＝28 摘要＋15 概念＋5 導覽＋9 教程＋5 合成工作紙。讀頁教學檢查初次 9/10，補 T05 後 10/10。最終 Lint 三類均 0，308 個正文連結有效；盲查另有失敗。 | `evidence/phase1c/teaching-checks.md` 第 5 題；`evidence/phase1c/final-report.md`「查核與結果」 |
| 2A｜編成五章 | 曾逐題對 110 個候選標題執行 `wiki_query`，76 個零命中；改按路徑讀 62 頁，比對主張與限制。早期 79 頁是提案。最終五章書稿及導論、總結有 98 筆核准內容與第二章新增 8 項，合計 106 筆要求、65 核心單元。 | `evidence/phase2a/phase2a-check-report.md`「來源核對與判讀」；`evidence/phase2a-final/delivery-review.md` |
| 2B-0／0R／0R2 → 2B-1｜試作 | 0 版拆出四單元的十四個位置。0R 修 C03-02、02-A03-02，0R2 再修 C31-03、C52-02。2B-1 將這四個定稿做成互動 HTML，另十篇保留故事板。既有 Gate A 覆蓋、B 教學、C 瀏覽器的判斷限該批。 | `docs/phase2b-1/storyboards/coverage.csv` 323 列；`docs/phase2b-1/storyboard-to-html.csv` 46 列；`evidence/phase2b-1/acceptance.md` |
| 前版驗收｜二次查讀 | 按歷史回執配對檔案、檢查保存位元組，對照正式教材與指定閱讀順序。這次未重跑歷史 MCP；本報告提交的是史料查核。 | [保存與重查](#preserve)；最終全書 Gate 和人類簽收另行判定 |

<a id="graph"></a>

## 從來源到驗收的靜態流程圖

```text
① 來源、作者、證據層級
 ↓
② 預演 → 正式匯入 → 逐頁讀回 ── 缺頁或截斷 ↺ ② 補摘要再讀
 ↓
③ 概念 ↔ 教程 ↔ 五章導覽 ───── 歸屬不明 ↺ ① 對原件
 ↓
④ Query → Read → 核對主張 ─── 零命中 ↺ ③ 修索引、重查並記結果
 ↓
⑤ 五章教材＋Manifest → 故事板 → HTML
 ↓
⑥ Gate A 逐項追溯 ────────── 缺反例或來源 ↺ ④／⑤
 ↓
⑦ Gate B 獨立跳讀 ────────── 看不懂代號 ↺ ⑤ 補前情
 ↓
⑧ Gate C 實際操作 ────────── 錯誤狀態或不可讀 ↺ ⑤ 修後重測
 ↓
⑨ Coordinator 核對本輪全書版本 → 人類判定
```

**回返與停點。** `docs/wiki-pipeline.md` 第 1–7 點記載：MCP 不可用先停；同一 Wiki 問題至多兩輪有依據的修正，仍失敗則記下影響。版本或研究歸屬互斥、需要新增資料或公開私人材料，交人類決定。下游編輯回返以受影響的單元重核；某一原型通過時只標記該版本、該範圍。⑨ 的判定依本輪正式交付紀錄。

<a id="query"></a>

## Query 找到什麼，Read 又支持什麼？

[打開查詢、讀回、Wiki 頁與教材對照](raw-evidence/index.html#query)

以下時間均為 2026-11-21 UTC。Query 回候選頁；審閱者再以指定頁正文與來源歸納答案。以下分開呈現成功與失敗，便於檢查改索引後的成績採用哪一組題目。

### 成功紀錄

- **可直接回查的技術界線。** 14:13:46.577，詢問 Git Worktree 解決什麼，唯一命中 `concepts/worktree.md`（9 分）。14:17:22.978 同題得到 P14 摘要（17 分）和概念頁（15 分）。`wiki_read_page` 對讀 P14 和 U-A：Git 文件支持各自 HEAD、index 及共享物件；版本權威與跨模組語義衝突屬使用者經驗。兩者同列在概念頁的「原理與工程用途」「適用條件與限制」。來源為 `evidence/query-validation.md` 第 4 題與對應概念頁。
- **一個整合多份來源的讀頁。** 1B 新題 2 比較工作區管理，目標 `concepts/tool-management.md` 排名 2 → 1 → 1。15:24:47.610 查詢，15:24:48.345 讀回。P06 支持以 session 選工作區，P12 支持以 worktree 管理工作區，P13 解釋 Task／Dispatch；個人的管理偏好另歸 S01。教師可檢查：文件能支持操作模式，若要宣稱某工具較快，仍缺同任務比較。見 `evidence/phase1b/query-validation.md` 新題 2、4。

### 失敗與另一次測試

- **指定題首輪漏查。** 14:13:46.979，詢問「人類不逐行審查程式碼時，如何建立工程驗證？」得 0 筆。用 `wiki_update_index` 增補索引，14:17:23.250 重問，唯一命中 `concepts/quality.md`（3 分）；正文與 P17、P20、U-C 支持以測試、驗收與風險抽查分層判斷。舊題曾進索引，只能計為指定題回歸。見 `evidence/query-validation.md` 第 9 題與「判定」。
- **自由問句仍然失敗。** 1C 的「畫面符合預期，但是請求到底送了什麼？」在 16:12:10.622 與 16:14:01.475 均為 0。另測「Browser 請求」：首輪未返回 T04，修索引後第 1；16:14:01.782 讀回 `tutorials/single-agent-coding-cycle.md`，正文用一筆符合、一筆不符合的資料區分篩選與清除。六題整句末輪 0/6，關鍵字末輪 6/6 首位；無候選時沒有可從該結果讀出的證據。見 `evidence/phase1c/query-blind-checks.md` 第 3 題。

<a id="chapters"></a>

## 從一項教學判斷跳回五章來源

以下按本輪 79 筆對照表標示閱讀序號，每章選一項可直接開啟的教學判斷。各列取自 `docs/textbook/evidence/book-coverage.csv` 的 requirement_id，舊版閱讀順序取自 `docs/phase2b-final/reading-plan.csv`。Wiki 定位均相對於 `.wiki/wiki/`。S007 等三位數是簡報需求，S01 等兩位數是來源。

| 章與教學判斷 | 來源 → Wiki → 正文（相對於 docs/textbook/） | 投影片或原型，與證據界線 |
|---|---|---|
| 第一章 · [1.03.02 Tool Calling 的執行生命週期與錯誤處理](../../../slides/book/index.html#C03-02)｜請求工具後，是否真的跑到了斷言？ | P02、P17 → T01 `tutorials/agent-system-model.md` → `ch01/C03-C08.md#c03` | S007／S008 → C03-02。拒絕權限、缺 fixture、斷言失敗各在不同步驟；示意請求編號屬教學例。 |
| 第二章 · [2.A.03.02 單 Agent 工程計畫：依重現結果調整修復步驟](../../../slides/book/index.html#02-A03-02)｜規劃器交給執行器什麼，何處應停？ | U04（收於 U-A）、T04 `tutorials/single-agent-coding-cycle.md` → `ch02/A-method.md#02-A03` | 第二章追加要求 02-A03 → 02-A03-02。讀者先有調查、重現、修改、複驗四步，再判讀停點；U04 是設計與交底，缺實跑軌跡。 |
| 第三章 · [3.10.03 Task DAG 案例：定位整合故障、重派與重驗](../../../slides/book/index.html#C31-03)｜API 已通過，整合票可否開始？ | P13、P01 → T06 `tutorials/requirements-to-delivery.md` → `ch03/organization-and-delivery.md#c31` | S063／S064 → C31-03。須先取得同一契約的 API 與 UI 兩份有效輸入；簽收還要重播故障。任務票及待辦資料為合成例。 |
| 第四章 · [4.08 Agent 失聯時的狀態查證與寫入權移交](../../../slides/book/index.html#C44)｜工作失聯時誰還持有修改權？ | P13、P28、U-B → T08 `tutorials/scheduling-supervision-handoff.md` → `ch04/C37-C46.md#c44` | S088／S089 → C44。從本章跳入先區分無心跳、已退出與等待批准；觀察分類是教法。2B-1 四個互動原型中無第四章，此處依正式書稿核對。 |
| 第五章 · [5.06.02 用六筆合成試次比較單 Agent 與多 Agent 的交付與成本](../../../slides/book/index.html#C52-02)｜能否用成功試次證明多 Agent 比較快？ | P20、U-C → T09 `tutorials/verification-efficiency-reuse.md` → `ch05/C47-C54.md#c52` | S104／S105 → C52-02。兩組各啟動 3 次，簽收各 2／1 次；雙方皆簽收的配對只有 1 對，相差 8 分鐘。六筆資料是合成示範。 |

查看全書的 [79 個閱讀入口](../reading-guide.html)，或從上表直接跳入五章教材。技術 ID 保留在原書稿路徑與追溯欄，方便複查。

<a id="repair"></a>

## 把查核放到下一步之前

[打開修正前後的三份紀錄](raw-evidence/index.html#loop)

**先讀回，再寫教材。** 1C 第 5 題問「API、UI 都要改共享型別，是否該加人？」16:12:10.091Z 讀 T05、16:12:10.331Z 讀 P14，原案例只有資料結構和 fixture，讀者無從判斷兩邊是否在改同一介面。編者先加入「字串陣列改成物件陣列」的反例，16:12:34.114Z 再讀回。教材因而能讓學生先定契約再評估並行；Git 文件仍只支持隔離機制。參見 `evidence/phase1c/teaching-checks.md` 第 5 題。

**先釐清狀態，再讓讀者操作。** 2B-1 的 C31 曾讓讀者先遇見 B0、K1 和派工代號。編輯退回後，先交代兩件待辦、正常結果、分責與版本表，才顯示互動。實際互動還暴露另一個錯誤：收到新嘗試 d2 的 ui-b，再按過期 d1，畫面竟將 UI 格退回「待補」。教師可對照下列兩筆去識別觀察。定位為 `evidence/phase2b-1/interaction-initial.json` 與 `interaction-final.json` 的 `C31-d1-d2-d1`。

| 歷史版本 | 收到 d2 後，舊 d1 按鈕仍啟用？ | 舊回報之後的有效配對 |
|---|---|---|
| 初測 | true | 退回 UI 待補，與已接受的 ui-b 矛盾 |
| 修訂複驗 | false | 保留 api-a ＋ ui-b；版本表已在互動前（afterVersionTable＝true） |

**反思。** 若只記「查得到」與「按鈕可用」，T05 的契約缺口和 C31 的狀態回退都會漏掉。可在製作下一頁前先問「哪一筆反例會改變結論」，在開下一張整合票前用「新回報後再送舊回報」檢查狀態是否倒退。歷史紀錄支持這兩次修正；節省多少工時、學生是否更容易學會，仍需獨立量測。

<a id="receipts"></a>

## 逐份匯入回執

[打開六份正式回執與讀回節錄](raw-evidence/index.html#ingests)

下表彙整 `wiki_ingest_with_context` 的實際回傳。所有時間均為 **2026-11-21 UTC**；每列依序給出成功預演、正式寫入及 1C 再讀回的時刻。每一正式列具 `status=success`、`dry_run=false`，產生一張摘要並更新 index.md、log.md。Wiki 相對頁名與完整 ISO 時戳可在 [逐份回執 CSV](source-receipts.csv) 比對。公開連結供查收錄來源；離線判讀只需本表。私人列只揭露整理主題與歸屬。

例如在 Phase 1 的 JSON Lines 搜尋 `2026-11-21T14:08:58.171Z`，下列四個欄位取自同一筆 P01 的 `result.ingest`。對照表內的 P01，14:08:54.787 是它的預演。其他摘要也可用 ID 小寫組成 `sources/<id>-summary.md` 對照。

```json
{"status":"success","dry_run":false,"pages_created":["sources/p01-summary.md"],"pages_updated":["index.md","log.md"]}
```

| 階段／ID | 文件或整理主題與歸屬 | 預演 UTC | 正式 UTC | 讀回 UTC |
|---|---|---|---|---|
| 1／P01 | [Building effective agents](https://www.anthropic.com/engineering/building-effective-agents)（Anthropic Engineering） | 14:08:54.787 | 14:08:58.171 | 16:10:37.906 |
| 1／P02 | [Running agents](https://developers.openai.com/api/docs/guides/agents/running-agents)（OpenAI） | 14:09:11.247 | 14:09:14.442 | 16:10:37.906 |
| 1／P03 | [Architecture overview](https://modelcontextprotocol.io/docs/learn/architecture)（Model Context Protocol） | 14:09:17.399 | 14:09:19.796 | 16:10:37.906 |
| 1／P05 | [AGENTS.md](https://agents.md/)（AGENTS.md 專案） | 14:09:22.554 | 14:09:24.921 | 16:10:37.906 |
| 1／P13 | [Orchestration](https://orca.dev/docs/cli/orchestration)（Orca） | 14:09:27.844 | 14:09:30.381 | 16:10:37.906 |
| 1／P14 | [git-worktree](https://git-scm.com/docs/git-worktree)（Git 專案） | 14:09:33.318 | 14:09:36.248 | 16:10:37.906 |
| 1／P15 | [Key Concepts](https://teamtopologies.com/key-concepts/)（Team Topologies） | 14:09:38.886 | 14:09:41.578 | 16:10:37.907 |
| 1／P17 | [Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)（Ryan Lopopolo／OpenAI） | 14:09:44.620 | 14:09:47.252 | 16:10:37.907 |
| 1／P20 | [Evaluate agent workflows](https://developers.openai.com/api/docs/guides/agent-evals)（OpenAI） | 14:09:50.251 | 14:09:53.223 | 16:10:37.907 |
| 1／U-A | AI 工程與多 Agent 工作流程（使用者研究，Codex 轉述） | 14:09:56.045 | 14:09:59.218 | 16:10:37.907 |
| 1／U-B | 多 Agent 實務決策（使用者研究，Codex 轉述） | 14:10:05.818 | 14:10:08.736 | 16:10:37.907 |
| 1／U-C | 工程驗證與效率研究（使用者研究，Codex 轉述） | 14:10:14.525 | 14:10:17.385 | 16:10:37.907 |
| 1B／P06 | [Use the Agents window](https://code.visualstudio.com/docs/agents/run/agents-window)（Microsoft／OpenAI） | 15:20:08.745 | 15:20:13.343 | 16:10:37.906 |
| 1B／P08 | [Antigravity documentation overview](https://antigravity.google/docs/overview)（Google） | 15:20:18.656 | 15:20:21.807 | 16:10:37.906 |
| 1B／P10 | [Models](https://antigravity.google/docs/models)（Google） | 15:20:24.912 | 15:20:27.824 | 16:10:37.906 |
| 1B／P12 | [Worktrees](https://orca.dev/docs/model/worktrees)（Orca） | 15:20:30.739 | 15:20:33.474 | 16:10:37.906 |
| 1B／P16 | [Agent orchestration](https://openai.github.io/openai-agents-python/multi_agent/)（OpenAI Agents SDK） | 15:20:36.556 | 15:20:39.223 | 16:10:37.907 |
| 1B／P24 | [Introducing the Codex app](https://openai.com/index/introducing-the-codex-app/)（OpenAI） | 15:20:42.119 | 15:20:44.694 | 16:10:37.907 |
| 1B／P25 | [Moving to the new ChatGPT desktop app](https://help.openai.com/en/articles/20001276-moving-to-the-new-chatgpt-desktop-app)（OpenAI） | 15:20:47.743 | 15:20:51.002 | 16:10:37.907 |
| 1B／P28 | [Tracing](https://openai.github.io/openai-agents-python/tracing/)（OpenAI Agents SDK） | 15:20:53.943 | 15:20:56.880 | 16:10:37.907 |
| 1B／S01 | 工具管理比較（使用者提供的補充教材） | 15:20:59.538 | 15:21:02.708 | 16:10:37.907 |
| 1B／S02 | 組織生命週期（使用者提供的補充教材） | 15:21:05.657 | 15:21:08.565 | 16:10:37.907 |
| 1B／S03 | 分層資訊管理（使用者提供的補充教材） | 15:21:11.646 | 15:21:14.561 | 16:10:37.907 |
| 1B／S04 | 工程證據與回報（使用者提供的補充教材） | 15:21:18.619 | 15:21:21.579 | 16:10:37.907 |
| 1B／S05 | 長期工程能力（使用者提供的補充教材） | 15:21:24.905 | 15:21:27.845 | 16:10:37.907 |
| 1C／P04 | [Build skills](https://learn.chatgpt.com/docs/build-skills)（OpenAI） | 16:05:05.797 | 16:05:08.908 | 16:10:37.906 |
| 1C／P07 | [Use browser tools with agents](https://code.visualstudio.com/docs/agents/run/browser-tools)（Microsoft） | 16:05:12.755 | 16:05:17.254 | 16:10:37.906 |
| 1C／P30 | [Retrieval-augmented generation (RAG) in Foundry IQ](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview)（Microsoft Learn） | 16:05:20.835 | 16:05:25.127 | 16:10:37.907 |

回執定位依序為 `evidence/ingest-log.md` 的 JSON Lines（Phase 1）、`evidence/phase1b/ingest-log.md` 的 JSONL（1B）、`evidence/phase1c/source-and-claim-audit.md` 的「新增三份原創摘要」（1C）。末欄讀回時間取自同一份 1C 文件「來源摘要讀回紀錄」。原紀錄中的 dry run 與正式回傳各 28 筆。ID 保留原編號，跳號的候選不計入。

<a id="preserve"></a>

## 保存、重查與證據缺口

**已驗證的保存範圍。** 2026-11-22 18:28（台北）以 Python `zipfile.ZipFile.testzip()` 查初始資料包，CRC 無錯；逐項比對 ZIP 成員與本機解壓檔，17/17 位元組相同，共 205,321 bytes。用 `hashlib.sha256` 回查 `evidence/phase2b-1/input-digests.json` 的 176 項，均符合舊基線，含 Wiki、來源與正式教材。另計算原型 HTML 的 SHA-256 為 `e70745575415b8c301de5fe1a78289ca771a92e52cb391411548a4b91fd1afd0`，與舊 Gate C 紀錄相同。完整性比對能查出這些已列檔案的變動；無法用雜湊還原未曾保存的資料。

**前版驗收逐項配對。** 解析上述三份 JSONL，檢查每個來源恰有一次成功預演與一次成功寫入、預期摘要檔和 index／log 更新欄位。28 個 ID 均能配對 1C 讀頁時戳與現存摘要檔；另按閱讀計畫的 79 列逐項核對 Markdown 明示錨點，65 核心＋14 細講全部找到。2A 先導另存 `evidence/phase2a-integration/C01-C02-verification.json`，當時記有 8 次唯讀 MCP 讀頁、核對 4 道原驗收題與 16 個相對連結。連結、檔案和時戳定位的成功不衡量讀者理解。

**本機查核方法。** 在完整專案可用下列唯讀指令調出五章落點與修前、修後欄位；教師在離線包可用 CSV 和本頁相應表格核對相同觀察。原始 ZIP、研究、私聊與機器專屬設定由保管者留在本機。第三方可重算所附 CSV 的數量；獨立查閱底層私人原件需要保管者協助。

```powershell
Import-Csv docs/textbook/evidence/book-coverage.csv | Where-Object requirement_id -in S007,02-A03,S063,S088,S104 | Select-Object unit_id,source_ids,textbook
Get-Content -Raw -Encoding UTF8 evidence/phase2b-1/interaction-final.json | ConvertFrom-Json | Select-Object -ExpandProperty C31-d1-d2-d1
Import-Csv docs/phase2b-final/assignment/source-receipts.csv | Group-Object phase | Select-Object Name,Count
```

**歷史歸屬與未決項。** U01／U02 為回溯摘要；U07 為使用者直接敘述；RBS v3 屬使用者的朋友。U05／U06 的 Dungeon Lab 功能測試只支持舊版本指定測項。U10 缺公式原文與前提；效率比較另缺同品質、同需求的對照試次。2A 終審還指出 S003 章表可能將 U-A 背景誤列為公開技術文件，查 C01 時應將該背景識別為歷史整理／轉述，公開機制另查 P01／P02。B0→B1、工作票與 C52 試次屬教學合成，U04 屬設計。來源為 `evidence/phase1c/source-and-claim-audit.md` 與 `evidence/phase2a-final/delivery-review.md`「本次發現與需決定的事項」。本報告未量測真人學習成效；全書交付與人類驗收留給該版紀錄。
