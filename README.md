# DecompAI #375: real Local Smoke on a combined SDK candidate

This export is one **custom** fixed Case, not official KUMA/GT or maintainer approval. The tested Agent unit was byte-identical to PR #436 head `14a04e447fec744e4e897cb987fe1e690751cf9e` (39 tracked files and 31 upstream source hashes). The runtime was current main `3b75d1a3f276a1c9ee338e4bd86c78543f50fdc2` plus `sdk-candidate.patch`; it was **not** the unmodified PR #436 runtime. The SDK patch in this archive is the exact one used in the run.

Case `local-decompai-branch-20261022-01`; run `e983ceb6a6594fc8b62d4facd56cbfba`; model `glm-5.3-flash`; case retries 0. Agent 2 HTTP-200 calls; Local Judge 1 call, `max_tokens=8192`, `reasoning_effort=low`, HTTP 200, finish `stop`; KUMA calls 0. Execution, host trace validation and cleanup succeeded; OTel complete with zero unfinished spans; derived trajectory complete with one exact observed tool link; Local Judge pass/high; CLI exit 0. The host Judge delivery is `received`; the unmodified SDK execution manifest says `not_requested` because the host performs the separate Judge step afterward.

Judge payload was 144709 characters and both trace hashes matched the source attachments. The 44 original request attachment hashes and request identity were verified; an independent byte-substring check verified the quoted disassembly. The Agent answered using actual observed output; the Local Judge remains a model judgment, not validated GT.

Environment: macOS arm64 host; Docker 29.8.1; Agent image linux/amd64; runtime memory 1 GiB, PID limit 128, 1 CPU as recorded in `request/execution-environment.json`. This 1-CPU main-SDK composition differs from the 2-CPU declaration supported by the PR #436 runtime changes. Build used cached original native layers, the disclosed public Python index mirror and an existing checked interceptor image. Agent source/tools were not changed.

Reported model costs: Agent USD 0.00184701; Judge USD 0.00730375; total USD 0.00915076, from provider usage. Original raw Judge request/response, source artifacts and network trace are included unchanged. `execution-summary.json` omits the private host output path; `audit-summary.json` is a derived index, not an original automatic manifest. Credentials, host-specific paths, SDK ledger and private resumable Judge context are excluded. Previous failed execution records are not changed by this export.

Run `python3 verify_evidence.py` after unpacking to verify the bound Judge request and every included file against the manifest.
