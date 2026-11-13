# Zaf report supporting evidence — 13 November 2026

This is a sharing package of existing research, not a forecast issuance or group sign-off. Source files are copied unchanged. Caches, installed dependencies, duplicate ZIPs and personal-device inventory are excluded.

## Evidence map
- Research instructions and dated action/tool record: `research/docs/research_transcript.md` (concise reconstruction, NOT a verbatim chat export), `research/docs/coursework_extracted.txt`, and `research/treasury_extension/RESEARCH_LOG.md`.
- Model decisions: `research/docs/model_specifications.md`, `research/treasury_extension/PROTOCOL.md`, research reports and reconciliation report.
- Original downloaded inputs, URLs, actual retrieval timestamps and hashes: `research/data/`, `research/sources/`, `research/treasury_extension/data/` and saved snapshots. Observation time does not establish first publication time.
- 52-origin forecasts and sensitivities: `research/results/`; corrected code: `research/src/`.
- 59-origin A/B/C comparison: `research/treasury_extension/results/all_forecasts.csv`, variant `primary`. Other variants are sensitivity analyses, not extra independent trials.
- Timing corrections: `research/pit_audit/AUDIT_REPORT.md`, `code_changes.diff`, `before/`, per-row ledgers and validation logs. Corrected 36 summer origin times and 197 delayed-label timestamps; numerical forecasts unchanged.
- Independent checks: `research/validation/`, `research/pit_audit/validation/`, `research/treasury_extension/validation/`. `INDEPENDENT_METRICS.json` is a fresh Decimal recalculation from preserved forecasts, not a refit.
- Live trial instructions, raw inputs/outputs and approvals: the four existing `../Zaf_Trial_0*_Evidence.zip` archives in GitHub zaf. Selected approval records are copied here; complete receipt context remains in those archives.
- Consolidation and provenance caveats: `research/reporting/2026-11-09/`. Those dated reports describe the status THEN; later addenda supersede their pending-outcome comments.

## Approval statement: qualified, not certified
The evidence package contains research instructions, dated source/tool records, model decisions, audit corrections and independent checks. Saved user-in-chat approvals concern particular trial source substitutions and issuances. **No evidence located establishes that all group members reviewed these records and approved the final submitted calculation.** Do not quote that second sentence as an accomplished fact. Final named reviewers, calculation identifier/hash, decision and actual approval timestamps remain pending. Upload approval is not forecast approval. Message-send timestamps absent in original records remain absent; no timestamps are backdated.

## Report labels versus frozen labels
- A: random walk; B: fixed 0.25 × 20-session simple momentum.
- Report C(i) = archived Zaf C: expanding simple-return momentum OLS, Friday origins, exact six-session labels.
- Report C(ii) = Artemis rolling three-year log-return momentum OLS, weekday matched, original 4–6-session labels.
- Report D = Artemis momentum + VIX OLS. **Archived Zaf D in the Treasury extension is a different Treasury-yield model. Its results are NOT evidence for report D.** No frozen files or labels have been renamed.
- The 52/59 results here back A/B/C(i), not unmatched historical superiority over C(ii) or VIX D. Existing Artemis trial records supply their live results.

## Reproduction
Extract to a NEW scratch directory before running scripts, since original scripts write outputs. Keep this evidence copy unchanged. Follow `research/README.md` and `research/treasury_extension/README.md`; install pinned `research/requirements.txt` into `research/vendor` in the scratch copy. Python 3.14.6 was originally used; matplotlib is additionally required only for chart/report generation. No AI account or new market download is needed.

Run `python3 research/src/run_backtest.py`, `python3 research/src/test_backtest.py`, `python3 research/src/audit_point_in_time.py`, `python3 research/src/test_point_in_time.py`, then `python3 research/treasury_extension/calculate.py` and `python3 research/treasury_extension/test_extension.py`. Do not run optional source-retrieval commands to reproduce historical evidence. Legacy comparison requires the legacy script outside this curated package and is not needed for the report's primary results.

## Limits and integrity
The 52/59 evaluation dates differ, but the latter reuses a previously explored training period. Weekly targets and October/live windows overlap; do not count them as independent experiments. Historical FRED first-publication times, revisions and direct official closing-record certification remain unresolved. Successful tests do not certify historical vintages. Provider redistribution restrictions remain applicable; this package grants no additional licence.

SHA256.json authenticates this package's included files (excluding itself). SOURCE_COPY_MANIFEST.json maps unchanged source copies. Older nested manifests are archival: absolute paths, omitted cache references and pre-audit path gaps are documented in the consolidation audit; no universal nested-manifest pass is claimed. Full original chat exports and final group sign-off are not supplied.
