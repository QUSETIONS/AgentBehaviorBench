# PR436 final-head review follow-up (2026-10-23)

Exact maintainer source head: `c7d825b0c7b32ada2a770aba17ba80d3aadc658c`; source tree `c830014b4ebf1967946d0e2c8a9b398a0979e61f`. This is a new local validation of the final head, not a new official KUMA run and not a rewrite of historical official results.

## Actual results

- Source synchronized by verified public GitHub Git object IDs and ordinary fast-forward; no synthetic/amended commit. A separate clean local checkout uses the exact same commit/tree. The documented bundled source was rebuilt from31 audited pinned regular files; native source, prompts, graph and18 tools remain unchanged. The known absolute runtime alias remains an empty directory. No fresh upstream network clone is claimed.
- Fresh host environment: Python3.12.14 / kuma-defuzex0.3.8. Exact review test selection: `151 passed, 5 skipped, 1 warning in 130.92s (0:02:10)`. Existing LangChain async/deprecation warnings were retained; skips are not passes.
- Unchanged committed Docker recipe plus standard ABB worker overlay built successfully,exit0. No custom build arguments, alternate recipe, privilege expansion or fabricated tool output. Offline container preflight actually executed objdump,structured native disassembly,strings,radare2 and Ghidra;exit0,network none,model/API calls0.
- Clean-checkout real Local Smoke: `run_22023cb13c774337b8079ca2fa2e7248`; Case `local-decompai-branch-20261022-01`. Execution succeeded,OTel and SDK Trace complete,unfinished spans0,Local Judge pass,CLI quality gate passed,exit0. Model: only opencode/glm-5.3-flash;2 Agent calls,all HTTP200;2 actual native tool results;one separate glm-5.3-flash Local Judge call. No fallback or automatic Case retry. One initial pre-execution SDK image build failed before any Agent/Judge call; it is preserved. Original source file modes were restored in the clean bundled copy; a diagnostic-only copy that merely prints failure logs completed the same native prewarm. The default committed recipe was then used for one explicit manual setup retry, not the diagnostic image. The original prewarm failure root cause is not established, and is not misattributed to the unused publish script executable-bit difference.
- Native Agent limits remain the committed defaults:{'pids-limit': '128', 'memory': '1g', 'cpus': '2.0', 'timeout_seconds': 1800}. The host Local Judge uses HTTPX only as a one-call transport for the exact original relay request bytes/prompt/schema/parser/verdict; no shared SDK/Judge source modification. Original request/prompt/source hashes are retained.
- KUMA API calls/Credits consumed0: only SDK local was invoked; no KUMA key loaded or official generation/judging performed. Model API use is not claimed to be free.
- PR-body automatic close changed from Closes to Refs. Baseline,modified and independent-copy rollback metadata tests preserve the original body hash; live PR retains ordinary association. Code is unchanged from the maintainer head.

## Remaining team decisions

Credits confirmation requested at https://github.com/DefuzeX-AI/AgentBehaviorBench/issues/375#issuecomment-6358287171. This request is not approval. Historical low-severity report-quality GT/finding acceptance and PR merge remain team decisions; no self-approval/merge or full acceptance claim.

## Archive

`DecompAI_c7d825b_LocalSmoke_Review_20261023.zip`;SHA256 `cabf69a86d71b567f104e227f331534b7b965f74a3f657b5200d085db8c4a5fe`;124 members,CRC pass,known actual credential matches0. Includes original automatic manifest/SDK Trace,network/egress,Agent output,Local Judge and execution/build/test provenance. Credentials,private SDK ledger,resumable Judge context and duplicate replay/channel data are excluded. The local fixture is custom,not official. File-capture flags remain as actually recorded; complete Trace does not invent file snapshots.
