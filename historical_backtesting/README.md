# Shared historical backtesting

Upload each member’s backtesting into a separate folder here on main, for example zaf/, artemis/ or orainna/. Only zaf/ is currently populated by this upload; other members can add their own folders.

## Add your evidence
1. Open this folder on GitHub and choose Add file → Create new file.
2. Name the file your_name/README.md; describe your models, sample periods and reproduction steps, then commit to main (or use a pull request).
3. Open your new folder and choose Add file → Upload files to add scripts, input snapshots, results and checksums. For many files, upload a ZIP plus a readable summary and checksum.
4. Keep other members’ files intact. Save corrections as a new dated version; do not overwrite frozen runs.

Include exact feature/return formulas, fitted versus fixed coefficients, expanding/rolling window rules, training weekdays, target horizons, label-maturity gates, sources and availability caveats, forecast/error tables and independent checks. Record observation/retrieval timestamps without inventing first-publication times. Exclude credentials and unrelated personal files; retain applicable source licences.

## Current contributions
- [Zaf historical backtesting](zaf/): 52-origin and 59-origin results, original input snapshots, scripts, timing audit, tests and reproduction guide.

Model labels alone do not establish equivalence. Report C(i) is Zaf expanding simple-return OLS; C(ii) is Artemis rolling log-return OLS; report D is Artemis VIX OLS. Archived Zaf Treasury Model D is different. Compare matched dates/horizons and do not pool overlapping samples as independent evidence. Historical backtests remain separate from live trials and binding forecasts.
