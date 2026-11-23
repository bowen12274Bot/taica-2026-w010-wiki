# 歷史 Wiki 與教材查核附件

[返回教師報告](../report.md) · [28 份回執總表](../source-receipts.csv) · [來源與證據分類](classification.html) · [雜湊與行號清單](manifest.json)

28 份來源的總表收錄 20 份公開文件整理與 8 份私人研究或補充整理。本附件從三個階段各選兩份公開來源，封裝 6 筆正式匯入及其讀回定位。其餘 22 份可在總表查閱回執欄位。

下列每個 .txt 只含所列原檔行，以 1 起算且含首尾，依列出順序拼接並保留原換行位元組。去敏方式一律為整行選取，省略其他行，所選行內無改寫。私人文件、對話、憑證與本機絕對路徑留在原專案。公開來源作者見回執總表。

整理時間為 2026-11-22T19:51:44+08:00（台北）。歷史工具時間採紀錄的 UTC。兩份查詢附件為當時的驗證紀錄，證明其記載的查詢、讀頁與判讀；本次未定位到該查詢的逐封 MCP 傳輸紀錄。現存 Wiki 頁用於內容比對，無法還原舊讀回的每一位元組。

<a id="ingests"></a>

## 核對六份正式匯入

先從總表按來源 ID 配對 formal_utc，再開相同行的歷史回執。檢查 dry_run 為 false、status 為 success，以及建立的摘要頁。最後核對六頁讀回紀錄。Phase 1 保存巢狀工具回應，1B、1C 的歷史檔保存扁平化回傳欄位。

### [P01｜Building effective agents](ingest-p01.txt)

正式工具回執。2026-11-21T14:08:58.171Z。Phase 1 的 wiki_ingest_with_context。Anthropic Engineering 的公開文件整理，回執建立 sources/p01-summary.md 並更新索引與日誌。後續讀回見「六頁摘要讀回」原檔第 38 行。

原檔 `evidence/ingest-log.md，行 27`

原檔 SHA-256 `5a3d9d00243c27e2524705cb65a3de385384a64ac32797d163f42496976a02c3`

節錄 SHA-256 `8fdb693cd0b16bae631153c3c2079d4367ee65824bbe0cf0c4b92495ccc54fe4`

### [P02｜Running agents](ingest-p02.txt)

正式工具回執。2026-11-21T14:09:14.442Z。Phase 1 的 wiki_ingest_with_context。OpenAI 的公開文件整理，回執建立 sources/p02-summary.md 並更新索引與日誌。後續讀回見「六頁摘要讀回」原檔第 39 行。

原檔 `evidence/ingest-log.md，行 29`

原檔 SHA-256 `5a3d9d00243c27e2524705cb65a3de385384a64ac32797d163f42496976a02c3`

節錄 SHA-256 `31200e3cf694b1744cc9b63c49dff53e34d4f51457702e3cd652a11c06b41598`

### [P06｜Use the Agents window](ingest-p06.txt)

正式工具回執。2026-11-21T15:20:13.343Z。Phase 1B 的 wiki_ingest_with_context。Microsoft／OpenAI 的公開文件整理，回執建立 sources/p06-summary.md 並更新索引與日誌。後續讀回見「六頁摘要讀回」原檔第 43 行。

原檔 `evidence/phase1b/ingest-log.md，行 23`

原檔 SHA-256 `975d715c11601225c7d61020855145a71bfdf9b1504a59938145a837a057f142`

節錄 SHA-256 `615d2d4cd9332e0b636c3b3904633fd8984824655afba385c1efe7903bc99d2c`

### [P12｜Worktrees](ingest-p12.txt)

正式工具回執。2026-11-21T15:20:33.474Z。Phase 1B 的 wiki_ingest_with_context。Orca 的公開文件整理，回執建立 sources/p12-summary.md 並更新索引與日誌。後續讀回見「六頁摘要讀回」原檔第 47 行。

原檔 `evidence/phase1b/ingest-log.md，行 29`

原檔 SHA-256 `975d715c11601225c7d61020855145a71bfdf9b1504a59938145a837a057f142`

節錄 SHA-256 `ad8e05d2120437195c75386ccd13a8dfd6cff4cf56392f8fa3bbcce813719283`

### [P04｜Build skills](ingest-p04.txt)

正式工具回執。2026-11-21T16:05:08.908Z。Phase 1C 的 wiki_ingest_with_context。OpenAI 的公開文件整理，回執建立 sources/p04-summary.md 並更新索引與日誌。後續讀回見「六頁摘要讀回」原檔第 41 行。

原檔 `evidence/phase1c/source-and-claim-audit.md，行 29`

原檔 SHA-256 `4fd32afbb9fb7b59038c46360edabddf4ecf06836aa134b880b1fe38fae6cee5`

節錄 SHA-256 `6344d7947a4f1ed3cee6a0a98a755cc5249f38d390a6bd95aa3f11b5553151a0`

### [P07｜Use browser tools with agents](ingest-p07.txt)

正式工具回執。2026-11-21T16:05:17.254Z。Phase 1C 的 wiki_ingest_with_context。Microsoft 的公開文件整理，回執建立 sources/p07-summary.md 並更新索引與日誌。後續讀回見「六頁摘要讀回」原檔第 44 行。

原檔 `evidence/phase1c/source-and-claim-audit.md，行 31`

原檔 SHA-256 `4fd32afbb9fb7b59038c46360edabddf4ecf06836aa134b880b1fe38fae6cee5`

節錄 SHA-256 `8241e491030f8383a3ecf89c31006850e1aeb6cdd11f1614cbdc37571266fdb7`

### [六頁摘要讀回](read-six.txt)

歷史讀回紀錄。2026-11-21T16:10:37.906Z。逐頁列出摘要位置、當時讀得的字元數與公開來源定位。六個時戳均與總表相符。

原檔 `evidence/phase1c/source-and-claim-audit.md，行 38, 39, 41, 43, 44, 47`

原檔 SHA-256 `4fd32afbb9fb7b59038c46360edabddf4ecf06836aa134b880b1fe38fae6cee5`

節錄 SHA-256 `c05a51fea4b9740ea4bd42061f75e3f0814cde3f4eef365787f0e48a8dc0638c`

<a id="query"></a>

## 從查詢結果回到教材引用

1B 的工作區比較保留查詢及讀頁兩個時間。1C 的瀏覽器問題保留原句失敗與改查之後的讀頁依據。循後一條鏈查讀，原句零命中 → 補索引後關鍵字命中 T04 → 讀頁要求先顯示兩筆資料 → 教材 2.B.03 明列 T04 並要求清除篩選後再驗兩筆。最後一步是本輪回查已驗收教材所作的映射。

[開啟教材 2.B.03 瀏覽器觀測](../../../../slides/book/index.html#C19) · [比較 2.B.05 工作階段](../../../../slides/book/index.html#C11)

### [比較工作區的查詢與讀頁](session-query.txt)

歷史驗證紀錄。2026-11-21T15:24:47.610Z 查詢；15:24:48.345Z 讀頁。wiki_query 的末輪首項為 concepts/tool-management.md。wiki_read_page 讀回後，記錄者分列 P06、P12、P13 的操作差異。題目曾進入索引。

原檔 `evidence/phase1b/query-validation.md，行 3, 13–19`

原檔 SHA-256 `2ad6225dbd22a3277424b616679abfdcc333253403e99d77858f83b238c7182a`

節錄 SHA-256 `b3978b90706909b5fd7f8852fe2f71524dde6bba362842114d5fea6ef189235a`

### [概念頁列出的兩種工作區入口](session-wiki.txt)

現存 Wiki 頁。頁面 created 為 2026-11-21T15:22:08.701Z；節錄取本輪保存版本。保留 P06 和 P12、P13 的兩行公開技術整理，供對照讀回判斷。頁面建立時間只定位版本歷程。

原檔 `.wiki/wiki/concepts/tool-management.md，行 25, 28`

原檔 SHA-256 `320ff78cf50c96fa87d98ad1fe4743f20f5572e149db27a7848b79c1dafd481f`

節錄 SHA-256 `9d7327a6cda04aa086e1c1c013d7e4c10d4c1dba3abc412322cbbd9d033f40e9`

### [原句失敗、關鍵字重查與 T04 讀回](browser-query.txt)

歷史驗證紀錄。2026-11-21T16:12:10.622Z 首查；16:14:01.475Z 原句複驗；16:14:01.782Z 讀回。索引補入來源事實及步驟。原句複驗仍為零筆，改查「Browser 請求」後 T04 由未返回升至第一名（6 分）。歷史紀錄未單列關鍵字查詢的毫秒時戳。

原檔 `evidence/phase1c/query-blind-checks.md，行 3, 17–21`

原檔 SHA-256 `2db96b040975618a058324b79bc8fff45a9f87c160cc54a611d45354518b0228`

節錄 SHA-256 `5655ea09278807b2e8a0f95d47ff15dd0b822cdbac62a0c0d13538438d6e9909`

### [T04 的反例與判斷依據](browser-wiki.txt)

現存 Wiki 頁。頁面 created 為 2026-11-21；節錄取本輪保存版本。教材設計的可反駁條件是先用兩筆資料建立基線，再檢查請求、篩選與清除。案例資料及預期屬合成教學。

原檔 `.wiki/wiki/tutorials/single-agent-coding-cycle.md，行 24, 36`

原檔 SHA-256 `8e0593cfdc6b2d75d6d12a1f0295f1f4461d525623e300b66b5e245b759aab36`

節錄 SHA-256 `c2cd8f5ad5b30f6e7456843aab525a119b2aec6783123c200ed648cfb4c18d8a`

### [教材明列 T04 的引用段落](browser-textbook.txt)

教材事後映射。4b61e62 已驗收教材；本輪查對，無歷史工具時戳。第二章 2.B.03（資料 ID C19）的判斷題明列 T03、T04、P07 等依據。學生必須排除「原本就只有 A」的解釋。

原檔 `docs/textbook/ch02/B-environment.md，行 53`

原檔 SHA-256 `e70bdd5c6506dc0771444ead779b678b59ab6aeda1ea54de4bac33ada1f48641`

節錄 SHA-256 `f3007fbdd30ee8562ab0e14be349e2236008441e863e8f029a714002b1a8beb0`

<a id="loop"></a>

## 在下一步之前驗出錯誤

T05 初讀缺少能判斷共享型別的反例，編者補例後再次讀頁。到了互動原型，初測發現過期 d1 能使已接受的 ui-b 退回待補。複驗時原按鈕已停用，after 保留有效配對。前一次驗教材能否支撐推理，後一次驗實際互動狀態。

### [共享型別反例的修正及讀回](teaching-loop.txt)

歷史教學驗證紀錄。2026-11-21T16:12:10.091Z／16:12:10.331Z 初讀；16:12:34.114Z 複讀。編排教材前先測能否用 T05 解題。初稿缺少共享型別改變的具體後果，加入反例再讀回，保留修正前判定。

原檔 `evidence/phase1c/teaching-checks.md，行 37–43`

原檔 SHA-256 `105fcbb923cab6b5d0ae1593203d29e09198080cfc31bc108e78c5a144e58cce`

節錄 SHA-256 `f96a61dc0bc231f4ac7e9c9a6173f293766a16e49adab9e559f543468c8089a8`

### [過期回報按鈕的初測](interaction-initial.txt)

歷史互動驗收輸出。Phase 2B-1 初測；JSON 未記錄執行時分秒。JSON 物件 /C31-d1-d2-d1。依次取得過期 d1、新 d2、再試舊 d1 後，對照 lateControlActiveAfterD2 和 after，核對舊回報能否覆蓋有效配對。

原檔 `evidence/phase2b-1/interaction-initial.json，行 36–41`

原檔 SHA-256 `5f3433fae3152e508f124b2ab77b16f5710851f1578d043de486dc17fae741df`

節錄 SHA-256 `a9467a96341587104fecea9289486ddb97c9229e5684a6e50849b0b1bab96763`

### [過期回報按鈕的複驗](interaction-final.txt)

歷史互動驗收輸出。Phase 2B-1 複驗；JSON 未記錄執行時分秒。JSON 物件 /C31-d1-d2-d1。依次取得過期 d1、新 d2、再試舊 d1 後，對照 lateControlActiveAfterD2 和 after，核對舊回報能否覆蓋有效配對。

原檔 `evidence/phase2b-1/interaction-final.json，行 36–41`

原檔 SHA-256 `d672c8808899f1e4bdf1e8f38a6651a4ae75c28a482fc9685e1162372882114d`

節錄 SHA-256 `e25532ab8ec2db7d6da8e39b504f5b1acf92f97251b7d8d739645a7919334f1e`

教師可在附件目錄執行 Get-FileHash -Algorithm SHA256 *.txt，與清單的 excerpt_sha256 比對。持有原檔者另可比對 source_sha256，再按 lines 重取原字節。兩種雜湊各自對應一份檔案。

## 本輪核對結果

已驗證：以 Python 對 15 份節錄逐一重取清單所列行，用 hashlib.sha256 比對原檔與附件，15 份位元組均相符。逐筆解析 JSONL，28 個來源各有一次成功預演和正式寫入，且與 1C 讀回列相符。已對照 79 筆附件序號的資料 ID 與基線全書順序；另以 git show 4b61e62:docs/textbook/ch02/B-environment.md 核對第 53 行，確認 2.B.03 的原書稿明列 T04。
