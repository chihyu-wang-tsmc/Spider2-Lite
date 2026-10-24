# Spider2-Lite

**Source:** GitHub [`xlang-ai/Spider2`](https://github.com/xlang-ai/Spider2) @ `cafb867` (2026-08-12), `spider2-lite/` subtree only
**Downloaded:** 2026-10-24, file-by-file from `raw.githubusercontent.com` (`git clone` kept dropping)

Text-to-SQL, no train/test split.

`spider2-lite.jsonl` — **547 tasks** (`instance_id`, `db`, `question`, `external_knowledge`):

| Dialect | Tasks |
|---|---|
| BigQuery | 205 (bq 180 + ga 25) |
| Snowflake | 207 (sf_bq 189 + sf 18) |
| SQLite (local) | 135 |

`evaluation_suite/gold/`
- `sql/` — 256 reference queries (not every task has one)
- `exec_result/` — 1544 expected-result CSVs, covering all 547 tasks
- `spider2lite_eval.jsonl` — 547 comparison settings

`resource/documents` — the `external_knowledge` files · `resource/syntax` — BigQuery / Snowflake function docs

**Not downloaded:** `baselines/` and `resource/databases/` (cloud schema dumps). BigQuery / Snowflake need your own accounts; the SQLite DBs come from a Google Drive link in the upstream README. The two `*_credential.json` files are placeholders.

---

Snapshot kept for benchmark work; see [chihyu-wang-tsmc/code-benchmarks](https://github.com/chihyu-wang-tsmc/code-benchmarks) for the full benchmark index. Licensing follows the upstream source.
