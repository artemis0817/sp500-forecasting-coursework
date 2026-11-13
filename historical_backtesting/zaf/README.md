# Zaf historical backtesting

Download and extract Zaf_Report_Support_20261113.zip. This is the identical verified package also retained in /zaf; no original evidence has been changed. It includes source snapshots, scripts, parameters, training rules, per-origin forecasts, audit corrections, validation logs and reproduction instructions.

| Sample | Origins | A MAPE | B MAPE | C(i) MAPE |
|---|---|---|---|---|
| 52-origin primary | 18 July 2025–16 October 2026 | 1.447796% | 1.454056% | 1.425992% |
| 59-origin primary | 5 January 2024–20 June 2025 | 1.828480% | 1.833404% | 1.807673% |

A = random walk; B = fixed 0.25 momentum; report C(i) = archived Zaf C, expanding simple-return momentum OLS with Friday origins and exact six-session labels. Report C(ii) is Artemis rolling OLS; report D is Artemis VIX OLS. Archived Zaf D in the Treasury extension is a DIFFERENT Treasury-yield model and its scores must not be assigned to report D.

Inside the archive, start with README.md and research/README.md. The 52-origin evidence is in research/results and research/src. The 59-origin evidence is in research/treasury_extension/results/all_forecasts.csv (primary variant). Point-in-time corrections and tests are in research/pit_audit. Reproduce only in a fresh scratch copy because original scripts write output files. No new market download is needed.

The samples are retrospective and not independent untouched tests. Historical publication times and data vintages remain unresolved; sample dates, return conventions and horizons must be matched before comparing other members’ scores. No final model or binding forecast is selected here. Final group sign-off is not established by these files.

ARCHIVE_MANIFEST.json gives the ZIP checksum; the ZIP contains per-file SHA256.json. INDEPENDENT_METRICS.json contains independent Decimal recalculations. Existing /zaf trial archives remain in place.
